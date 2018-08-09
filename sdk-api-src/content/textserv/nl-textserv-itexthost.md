---
UID: NL:textserv.ITextHost
title: ITextHost
author: windows-sdk-content
description: The ITextHost interface is used by a text services object to obtain text host services.
old-location: controls\ITextHost.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itexthost.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITextHost, ITextHost interface [Windows Controls], ITextHost interface [Windows Controls],described, _win32_ITextHost, _win32_ITextHost_cpp, controls.ITextHost, controls._win32_ITextHost, textserv/ITextHost
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
req.header: textserv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TMGR_DIRECTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextHost
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextHost class


## -description


The <b>ITextHost</b> interface is used by a text services object to obtain text host services.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextHost</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITextHost</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITextHost</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6033e248-21e6-4c29-adb5-84db4aaa1f4d">OnTxCharFormatChange</a>
</td>
<td align="left" width="63%">
Sets the default character format for the text host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/695265ea-667b-4788-8bb0-eef7c3feb50e">OnTxParaFormatChange</a>
</td>
<td align="left" width="63%">
Sets the default paragraph format for the text host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ad31706-e5aa-49ea-8416-ce522fbdfbac">TxActivate</a>
</td>
<td align="left" width="63%">
Notifies the text host that the control is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7b54f78-ba7e-4ed2-b73f-acbead617743">TxClientToScreen</a>
</td>
<td align="left" width="63%">
Converts text host coordinates to screen coordinates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b7e1b5a3-3d63-4a52-8d48-42865bf1eef3">TxCreateCaret</a>
</td>
<td align="left" width="63%">
Creates a new shape for text host's caret.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7d102e1-4082-44aa-b930-a8dc371ed591">TxDeactivate</a>
</td>
<td align="left" width="63%">
Notifies the text host that the control is now inactive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88326109-7761-41cc-b55c-40f34d2ee3c1">TxEnableScrollBar</a>
</td>
<td align="left" width="63%">
Enables or disables one or both scroll bar arrows in the text host window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0658f73-edab-4540-a560-110e277b8d27">TxGetAcceleratorPos</a>
</td>
<td align="left" width="63%">
Requests the special character to use for the underlining accelerator character.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03decbb6-b272-4ba0-a902-013aa0dde18e">TxGetBackStyle</a>
</td>
<td align="left" width="63%">
Requests the background style of the text host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e98a8326-2a18-47e0-aa67-a5240dfcff91">TxGetCharFormat</a>
</td>
<td align="left" width="63%">
Requests the text host's default character format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b1d8dbf-73b7-4a0d-8bb0-14e506de6aaf">TxGetClientRect</a>
</td>
<td align="left" width="63%">
Retrieves the client coordinates of the text host's client area.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ffc852a-d179-4ea4-84f7-cd03043450ea">TxGetDC</a>
</td>
<td align="left" width="63%">
Requests the device context for the text host window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03cf4acc-f70e-40a4-9050-6e6777867b2b">TxGetExtent</a>
</td>
<td align="left" width="63%">
Requests the native size of the control in <b>HIMETRIC</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ae6f605-c845-40f1-a86d-1697570c1683">TxGetMaxLength</a>
</td>
<td align="left" width="63%">
Gets the text host's maximum allowed length for the text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ff0bb9f-85c5-4209-b9b8-e6107848e628">TxGetParaFormat</a>
</td>
<td align="left" width="63%">
Requests the text host's default paragraph format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2208eca-13f7-4ba3-a642-9c66e7e89f59">TxGetPasswordChar</a>
</td>
<td align="left" width="63%">
Requests the text host's password character.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/739367f6-01e0-4360-95ba-f22537c06967">TxGetPropertyBits</a>
</td>
<td align="left" width="63%">
Requests the bit property settings for the text host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f85a0786-41ad-4591-a62f-d2442e90b9a9">TxGetScrollBars</a>
</td>
<td align="left" width="63%">
Requests information about the scroll bars supported by the text host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17b91e0f-79db-4849-ac88-744402723046">TxGetSelectionBarWidth</a>
</td>
<td align="left" width="63%">
Gets the size of selection bar in <b>HIMETRIC</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7a81e26-196b-4ae1-b95e-c4e1f6effdd7">TxGetSysColor</a>
</td>
<td align="left" width="63%">
Gets the text host's color for a specified display element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/78f68d49-15b2-443a-a92a-d0c1c8d0e9e8">TxGetViewInset</a>
</td>
<td align="left" width="63%">
Requests the dimensions of the white space inset around the text in the text host window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1dcca568-e38c-42aa-a66f-0660bac6c0b6">TxImmGetContext</a>
</td>
<td align="left" width="63%">
The 
			<a href="https://msdn.microsoft.com/1dcca568-e38c-42aa-a66f-0660bac6c0b6">TxImmGetContext</a> method retrieves the IME input context associated with the text services host. 

This method is used only in Asian-language versions of the operating system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66923ce5-2bfb-4df0-a693-052b38ee5c7b">TxImmReleaseContext</a>
</td>
<td align="left" width="63%">
Releases an input context returned by the <a href="https://msdn.microsoft.com/1dcca568-e38c-42aa-a66f-0660bac6c0b6">TxImmGetContext</a> method and unlocks the memory associated with the context. 

This method is used only in Asian-language versions of the operating system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a1c1fc9f-3a77-495f-a73a-d60e0d84db1a">TxInvalidateRect</a>
</td>
<td align="left" width="63%">
Specifies a rectangle for the text host to add to the update region of the text host window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb3f01eb-1b95-49d7-9417-a29fb58d6805">TxKillTimer</a>
</td>
<td align="left" width="63%">
Requests the text host to destroy the specified timer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/304da32b-c80a-43b8-b240-14b2ac4aba80">TxNotify</a>
</td>
<td align="left" width="63%">
Notifies the text host of various events. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f6acad6e-2ae4-4d0c-b0ce-4ded27f6f8d4">TxReleaseDC</a>
</td>
<td align="left" width="63%">
Releases the device context obtained by the <a href="https://msdn.microsoft.com/8ffc852a-d179-4ea4-84f7-cd03043450ea">TxGetDC</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29823588-981c-4f6e-8371-8bb1a7d6860d">TxScreenToClient</a>
</td>
<td align="left" width="63%">
Converts the screen coordinates to the text host window coordinates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/47528256-8414-4b9b-a8db-cd33364b6b25">TxScrollWindowEx</a>
</td>
<td align="left" width="63%">
Requests the text host to scroll the content of the specified client area.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c82701e-ba79-4f11-b2bd-d480c6f8eb0f">TxSetCapture</a>
</td>
<td align="left" width="63%">
Sets the mouse capture in the text host's window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/11615426-8c97-4cd0-b0dc-58da8acc45d5">TxSetCaretPos</a>
</td>
<td align="left" width="63%">
Moves the caret position to the specified coordinates in the text host window. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab5b868e-816c-4122-99d2-4351f7ce3613">TxSetCursor</a>
</td>
<td align="left" width="63%">
Establishes a new cursor shape (I-beam) in the text host's window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18ae25c8-7eec-45f6-b3e7-fcdb350e8129">TxSetFocus</a>
</td>
<td align="left" width="63%">
Sets the focus to the text host window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d7432ba-927f-4ecd-9035-932fda8b5473">TxSetScrollPos</a>
</td>
<td align="left" width="63%">
Requests that the text host set the position of the scroll box (thumb) in the specified scroll bar and, if requested, redraws the scroll bar to reflect the new position of the scroll box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4df610f4-9fca-4516-93ff-fd91cd18be45">TxSetScrollRange</a>
</td>
<td align="left" width="63%">
Sets the minimum and maximum position values for the specified scroll bar in the text host window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8b4c691-d736-4ea0-ab90-4f271c283e25">TxSetTimer</a>
</td>
<td align="left" width="63%">
Requests that the text host create a timer with a specified time-out.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6fe417fd-a486-4e04-a613-71ab1ee320fa">TxShowCaret</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/6fe417fd-a486-4e04-a613-71ab1ee320fa">TxShowCaret</a> method shows or hides the caret at the caret position in the text host window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f72b7137-be70-4b4c-b9d4-cc3a65c9da60">TxShowScrollBar</a>
</td>
<td align="left" width="63%">
Shows or hides the scroll bar in the text host window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed32b64e-0f83-45b8-8c39-01975d4a9725">TxViewChange</a>
</td>
<td align="left" width="63%">
Indicates to the text host that the update region has changed.

</td>
</tr>
</table> 


## -remarks



You must implement the <b>ITextHost</b> interface before you call the <a href="https://msdn.microsoft.com/475ede7d-75ba-4eda-8253-1166fc9f45fe">CreateTextServices</a> function.

Applications do not call the <b>ITextHost</b> methods. A text services object created by the <a href="https://msdn.microsoft.com/475ede7d-75ba-4eda-8253-1166fc9f45fe">CreateTextServices</a> function calls the interface methods.




## -see-also




<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls Overview</a>
 

 

