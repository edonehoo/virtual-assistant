---
# Sidenav top-level section
# should be the same for all markdown files
section: PatternFly-AI
subsection: ChatBot
# Sidenav secondary level section
# should be the same for all markdown files
id: Messages
# Tab (react | react-demos | html | html-demos | design-guidelines | accessibility)
source: demo
sourceLink: https://github.com/patternfly/chatbot/blob/main/packages/module/patternfly-docs/content/extensions/chatbot/examples/demos/demos.md
---

import ChatbotToggle from '@patternfly/chatbot/dist/dynamic/ChatbotToggle';
import Chatbot, { ChatbotDisplayMode } from '@patternfly/chatbot/dist/dynamic/Chatbot';
import ChatbotContent from '@patternfly/chatbot/dist/dynamic/ChatbotContent';
import ChatbotWelcomePrompt from '@patternfly/chatbot/dist/dynamic/ChatbotWelcomePrompt';
import ChatbotFooter, { ChatbotFootnote } from '@patternfly/chatbot/dist/dynamic/ChatbotFooter';
import MessageBar from '@patternfly/chatbot/dist/dynamic/MessageBar';
import MessageBox from '@patternfly/chatbot/dist/dynamic/MessageBox';
import Message from '@patternfly/chatbot/dist/dynamic/Message';
import FileDropZone from '@patternfly/chatbot/dist/dynamic/FileDropZone';
import FileDetailsLabel from '@patternfly/chatbot/dist/dynamic/FileDetailsLabel';
import SourceDetailsMenuItem from '@patternfly/chatbot/dist/dynamic/SourceDetailsMenuItem';
import PreviewAttachment from '@patternfly/chatbot/dist/dynamic/PreviewAttachment';
import AttachmentEdit from '@patternfly/chatbot/dist/dynamic/AttachmentEdit';
import { BellIcon, CalendarAltIcon, ClipboardIcon, CodeIcon, UploadIcon } from '@patternfly/react-icons';
import { useDropzone } from 'react-dropzone';
import PFHorizontalLogoColor from '../UI/PF-HorizontalLogo-Color.svg';
import PFHorizontalLogoReverse from '../UI/PF-HorizontalLogo-Reverse.svg';
import ChatbotHeader, {
ChatbotHeaderMenu,
ChatbotHeaderMain,
ChatbotHeaderTitle,
ChatbotHeaderActions,
ChatbotHeaderSelectorDropdown,
ChatbotHeaderOptionsDropdown
} from '@patternfly/chatbot/dist/dynamic/ChatbotHeader';
import ChatbotAlert from '@patternfly/chatbot/dist/dynamic/ChatbotAlert';
import ExpandIcon from '@patternfly/react-icons/dist/esm/icons/expand-icon';
import OpenDrawerRightIcon from '@patternfly/react-icons/dist/esm/icons/open-drawer-right-icon';
import OutlinedWindowRestoreIcon from '@patternfly/react-icons/dist/esm/icons/outlined-window-restore-icon';
import PFIconLogoColor from '../UI/PF-IconLogo-Color.svg';
import PFIconLogoReverse from '../UI/PF-IconLogo-Reverse.svg';
import userAvatar from '../Messages/user_avatar.svg';
import patternflyAvatar from '../Messages/patternfly_avatar.jpg';

## Demos

### Attach via upload button in message bar

This demo displays unique attachment features, including:

1. [`<ChatbotContent>` and `<MessageBox>`](/patternfly-ai/chatbot/ui#content-and-message-box) components that contain:
   - An initial [user `<Message>`](/patternfly-ai/chatbot/messages#user-messages) with an attachment.
   - The ability to preview or edit the attachment using the [`<PreviewAttachment>` and `<AttachmentEdit>` components.](/patternfly-ai/chatbot/messages##file-attachments)
   - A [PatternFly `<Alert>`](/components/alert), customized to be sticky within the ChatBot window, which provides success or error messages for attachments.
2. `<ChatbotContent>` and `<ChatbotFooter>`, wrapped in a `<FileDropZone>` component to support drag and drop attachments. The footer also:
   - Displays attached files, using a [`<FileDetailsLabel>`](/patternfly-ai/chatbot/messages#attachment-label) component.
   - Demonstrates custom handling of file uploads, using the `handleAttach` in `<MessageBar>` and `handleFileDrop` in `<FileDropZone>`.

This demo includes broader ChatBot features, including:

1. A [`<ChatbotToggle>`](/patternfly-ai/chatbot/ui#toggle) that controls the [`<Chatbot>`](/patternfly-ai/chatbot/ui#container) container.
2. A [`<ChatbotHeader>`](/patternfly-ai/chatbot/ui#header) that updates based on the display mode, with sub-components (including a `<ChatbotHeaderTitle>`).
3. The ability to swap display modes via the `<ChatbotHeaderOptionsDropdown>`
4. A `<ChatbotContent>` and [`<MessageBox>`](/patternfly-ai/chatbot/uir#content-and-message-box) with:
   - A `<ChatbotWelcomePrompt>`
   - The ability to preview or edit the attachment.
   - An initial bot message
5. A [`<ChatbotFooter>`](/patternfly-ai/chatbot/ui#footer) with a [`<ChatbotFootnote>`](/patternfly-ai/chatbot/ui#footnote-with-popover) and a `<MessageBar>`

```js file="./ChatbotAttachment.tsx" isFullscreen

```

### Attach via menu of options in message bar

This demo displays unique attachment features, including:

1. [`<ChatbotContent>` and `<MessageBox>`](/patternfly-ai/chatbot/ui#content-and-message-box) components that contain:
   - A PatternFly [`<Alert>`](/components/alert) to provide success or error messages for attachments.
2. `<ChatbotContent>` and `<ChatbotFooter>`, wrapped in a `<FileDropZone>` component to support drag and drop attachments. The footer also:

   - Displays attached files, using a [`<FileDetailsLabel>`](/patternfly-ai/chatbot/ui#attachment-label) component.
   - Demonstrates custom handling of file uploads, using the `handleAttach` in `<MessageBar>` and `handleFileDrop` in `<FileDropZone>`.
   - Demonstrates how to define the `attachMenuProps` in the `<MessageBar>` to create a menu that allows users to select the source of an item they're attaching.

This demo includes broader ChatBot features, including:

1. A [`<ChatbotToggle>`](/patternfly-ai/chatbot/ui#toggle) that controls the [`<Chatbot>`](/patternfly-ai/chatbot/ui#container) container.
2. A `<ChatbotContent>` and [`<MessageBox>`](/patternfly-ai/chatbot/ui#content-and-message-box) with:
   - A `<ChatbotWelcomePrompt>`
   - An initial user message and initial bot message
3. A [`<ChatbotFooter>`](/patternfly-ai/chatbot/ui#footer) with a [`<ChatbotFootnote>`](/patternfly-ai/chatbot/ui#footnote-with-popover) and a `<MessageBar>`

```js file="./ChatbotAttachmentMenu.tsx" isFullscreen

```