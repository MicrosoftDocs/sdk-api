---
UID: NL:textserv.ITextHost
title: ITextHost
author: windows-sdk-content
description: The ITextHost interface is used by a text services object to obtain text host services.
old-location: controls\ITextHost.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itexthost.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
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
req.lib: 
req.dll: Msftedit.dll
req.irql: 
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
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/en-us/library/Bb787619(v=VS.85).aspx">OnTxCharFormatChange</a>
</td>
<td align="left" width="63%">
Sets the default character format for the text host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787625(v=VS.85).aspx">OnTxParaFormatChange</a>
</td>
<td align="left" width="63%">
Sets the default paragraph format for the text host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787636(v=VS.85).aspx">TxActivate</a>
</td>
<td align="left" width="63%">
Notifies the text host that the control is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787638(v=VS.85).aspx">TxClientToScreen</a>
</td>
<td align="left" width="63%">
Converts text host coordinates to screen coordinates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787640(v=VS.85).aspx">TxCreateCaret</a>
</td>
<td align="left" width="63%">
Creates a new shape for text host's caret.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787642(v=VS.85).aspx">TxDeactivate</a>
</td>
<td align="left" width="63%">
Notifies the text host that the control is now inactive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787644(v=VS.85).aspx">TxEnableScrollBar</a>
</td>
<td align="left" width="63%">
Enables or disables one or both scroll bar arrows in the text host window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787646(v=VS.85).aspx">TxGetAcceleratorPos</a>
</td>
<td align="left" width="63%">
Requests the special character to use for the underlining accelerator character.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787648(v=VS.85).aspx">TxGetBackStyle</a>
</td>
<td align="left" width="63%">
Requests the background style of the text host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787654(v=VS.85).aspx">TxGetCharFormat</a>
</td>
<td align="left" width="63%">
Requests the text host's default character format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787656(v=VS.85).aspx">TxGetClientRect</a>
</td>
<td align="left" width="63%">
Retrieves the client coordinates of the text host's client area.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787660(v=VS.85).aspx">TxGetDC</a>
</td>
<td align="left" width="63%">
Requests the device context for the text host window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787664(v=VS.85).aspx">TxGetExtent</a>
</td>
<td align="left" width="63%">
Requests the native size of the control in <b>HIMETRIC</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787669(v=VS.85).aspx">TxGetMaxLength</a>
</td>
<td align="left" width="63%">
Gets the text host's maximum allowed length for the text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787674(v=VS.85).aspx">TxGetParaFormat</a>
</td>
<td align="left" width="63%">
Requests the text host's default paragraph format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787691(v=VS.85).aspx">TxGetPasswordChar</a>
</td>
<td align="left" width="63%">
Requests the text host's password character.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787692(v=VS.85).aspx">TxGetPropertyBits</a>
</td>
<td align="left" width="63%">
Requests the bit property settings for the text host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787694(v=VS.85).aspx">TxGetScrollBars</a>
</td>
<td align="left" width="63%">
Requests information about the scroll bars supported by the text host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787696(v=VS.85).aspx">TxGetSelectionBarWidth</a>
</td>
<td align="left" width="63%">
Gets the size of selection bar in <b>HIMETRIC</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787698(v=VS.85).aspx">TxGetSysColor</a>
</td>
<td align="left" width="63%">
Gets the text host's color for a specified display element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787700(v=VS.85).aspx">TxGetViewInset</a>
</td>
<td align="left" width="63%">
Requests the dimensions of the white space inset around the text in the text host window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787702(v=VS.85).aspx">TxImmGetContext</a>
</td>
<td align="left" width="63%">
The 
			<a href="https://msdn.microsoft.com/en-us/library/Bb787702(v=VS.85).aspx">TxImmGetContext</a> method retrieves the IME input context associated with the text services host. 

This method is used only in Asian-language versions of the operating system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787704(v=VS.85).aspx">TxImmReleaseContext</a>
</td>
<td align="left" width="63%">
Releases an input context returned by the <a href="https://msdn.microsoft.com/en-us/library/Bb787702(v=VS.85).aspx">TxImmGetContext</a> method and unlocks the memory associated with the context. 

This method is used only in Asian-language versions of the operating system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787706(v=VS.85).aspx">TxInvalidateRect</a>
</td>
<td align="left" width="63%">
Specifies a rectangle for the text host to add to the update region of the text host window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787708(v=VS.85).aspx">TxKillTimer</a>
</td>
<td align="left" width="63%">
Requests the text host to destroy the specified timer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787710(v=VS.85).aspx">TxNotify</a>
</td>
<td align="left" width="63%">
Notifies the text host of various events. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787712(v=VS.85).aspx">TxReleaseDC</a>
</td>
<td align="left" width="63%">
Releases the device context obtained by the <a href="https://msdn.microsoft.com/en-us/library/Bb787660(v=VS.85).aspx">TxGetDC</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787714(v=VS.85).aspx">TxScreenToClient</a>
</td>
<td align="left" width="63%">
Converts the screen coordinates to the text host window coordinates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787716(v=VS.85).aspx">TxScrollWindowEx</a>
</td>
<td align="left" width="63%">
Requests the text host to scroll the content of the specified client area.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787718(v=VS.85).aspx">TxSetCapture</a>
</td>
<td align="left" width="63%">
Sets the mouse capture in the text host's window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787720(v=VS.85).aspx">TxSetCaretPos</a>
</td>
<td align="left" width="63%">
Moves the caret position to the specified coordinates in the text host window. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787681(v=VS.85).aspx">TxSetCursor</a>
</td>
<td align="left" width="63%">
Establishes a new cursor shape (I-beam) in the text host's window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787682(v=VS.85).aspx">TxSetFocus</a>
</td>
<td align="left" width="63%">
Sets the focus to the text host window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787683(v=VS.85).aspx">TxSetScrollPos</a>
</td>
<td align="left" width="63%">
Requests that the text host set the position of the scroll box (thumb) in the specified scroll bar and, if requested, redraws the scroll bar to reflect the new position of the scroll box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787684(v=VS.85).aspx">TxSetScrollRange</a>
</td>
<td align="left" width="63%">
Sets the minimum and maximum position values for the specified scroll bar in the text host window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787686(v=VS.85).aspx">TxSetTimer</a>
</td>
<td align="left" width="63%">
Requests that the text host create a timer with a specified time-out.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787687(v=VS.85).aspx">TxShowCaret</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/Bb787687(v=VS.85).aspx">TxShowCaret</a> method shows or hides the caret at the caret position in the text host window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787688(v=VS.85).aspx">TxShowScrollBar</a>
</td>
<td align="left" width="63%">
Shows or hides the scroll bar in the text host window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787689(v=VS.85).aspx">TxViewChange</a>
</td>
<td align="left" width="63%">
Indicates to the text host that the update region has changed.

</td>
</tr>
</table> 


## -remarks



You must implement the <b>ITextHost</b> interface before you call the <a href="https://msdn.microsoft.com/en-us/library/Bb787722(v=VS.85).aspx">CreateTextServices</a> function.

Applications do not call the <b>ITextHost</b> methods. A text services object created by the <a href="https://msdn.microsoft.com/en-us/library/Bb787722(v=VS.85).aspx">CreateTextServices</a> function calls the interface methods.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb787609(v=VS.85).aspx">Windowless Rich Edit Controls Overview</a>
 

 

