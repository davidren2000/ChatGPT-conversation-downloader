Ver 2.0 更新说明
更新说明
更新内容
新增了自动滚动到底部功能，确保完整加载所有对话内容。
优化了用户提问（User Message）与ChatGPT回答（Assistant Message）的识别逻辑，适配新版ChatGPT网页结构。
支持长对话提取，避免因懒加载（Lazy Load）导致只抓取部分对话的问题。
文件命名仍支持自动读取对话标题，若无法获取则提示用户手动输入。
增强了异常处理与兼容性，确保脚本在不同浏览器环境下稳定运行。
更新原因
近期ChatGPT网页前端结构更新，且引入了虚拟滚动与懒加载机制，导致传统的静态DOM抓取方法无法获取完整对话。
尤其在长对话场景下，未加载到可视区域的内容不会出现在HTML结构中，因此必须先模拟自动滚动，等待全部内容动态加载后，才能确保完整提取。
本次更新针对以上变动进行了修正，提升了脚本的适应性与可靠性。
Update Notes
What's Updated
Added auto-scroll to bottom functionality to ensure full conversation loading.
Improved User Message and Assistant Message recognition to adapt to the new ChatGPT webpage structure.
Supported long conversation extraction, avoiding missing content due to lazy-loading mechanisms.
File naming still supports auto-fetching the conversation title; if unavailable, prompts user input.
Enhanced error handling and compatibility across different browser environments.
Why Updated
Recently, ChatGPT's frontend introduced virtual scrolling and lazy loading, meaning not all conversation data is present in the DOM unless manually scrolled into view.
In long conversations, previous static scraping methods could only capture partial content.
This update fixes the issue by automatically scrolling the page to trigger dynamic content loading, ensuring complete and accurate extraction of both user questions and ChatGPT responses.



Ver1.0 
脚本介绍
  这段脚本可以帮助用户从当前浏览器窗口中，自动提取ChatGPT对话内容，并以当前对话标题命名保存为 .txt 文件。
  主要功能包括：
  自动滚动到页面顶部，确保加载完整对话历史。
  自动区分每条信息是用户发言还是ChatGPT回答。
  每条对话加上时间戳，便于后续整理和查阅。
  自动提取左侧对话列表中选中的对话标题作为文件名。
  如果无法自动获取标题，会提示用户手动输入，确保保存不失败。
  自动清理文件名中的非法字符，兼容所有操作系统。
  最终生成一个标准的 .txt 文件，供用户备份、整理、归档使用。
  适合需要备份重要对话、整理知识笔记、或者长期保存交流内容的用户使用。
  无需任何插件，只需打开浏览器控制台，即可一键运行。

📄 Script Description
  This script allows users to automatically extract the current ChatGPT conversation from the browser window and save it as a .txt file, using the current conversation title as the filename.
  Key features include:
  Automatically scrolls to the top of the page to ensure the entire conversation history is loaded.
  Clearly distinguishes between User messages and ChatGPT responses.
  Adds a timestamp to each message for easy reference and organization.
  Automatically fetches the selected conversation title from the sidebar to use as the filename.
  If the title cannot be retrieved automatically, it prompts the user to manually input one.
  Cleans illegal characters from the filename to ensure compatibility across all operating systems.
  Generates a neatly formatted .txt file for easy backup, organization, and archiving.
  This script is ideal for users who want to back up important conversations, organize knowledge notes, or preserve long-term records.
  No plugins are required — simply open the browser console and run it with one click.
