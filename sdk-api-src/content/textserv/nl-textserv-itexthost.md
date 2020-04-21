---
UID: NL:textserv.ITextHost
title: ITextHost (textserv.h)
description: The ITextHost interface is used by a text services object to obtain text host services.helpviewer_keywords: ["ITextHost","ITextHost interface [Windows Controls]","ITextHost interface [Windows Controls]","described","_win32_ITextHost","_win32_ITextHost_cpp","controls.ITextHost","controls._win32_ITextHost","textserv/ITextHost"]
old-location: controls\ITextHost.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itexthost.htm
ms.date: 12/05/2018
ms.keywords: ITextHost, ITextHost interface [Windows Controls], ITextHost interface [Windows Controls],described, _win32_ITextHost, _win32_ITextHost_cpp, controls.ITextHost, controls._win32_ITextHost, textserv/ITextHost
f1_keywords:
- textserv/ITextHost
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextHost class


## -description


The <b>ITextHost</b> interface is used by a text services object to obtain text host services.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextHost</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITextHost</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-ontxcharformatchange">OnTxCharFormatChange</a>
</td>
<td align="left" width="63%">
Sets the default character format for the text host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-ontxparaformatchange">OnTxParaFormatChange</a>
</td>
<td align="left" width="63%">
Sets the default paragraph format for the text host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txactivate">TxActivate</a>
</td>
<td align="left" width="63%">
Notifies the text host that the control is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txclienttoscreen">TxClientToScreen</a>
</td>
<td align="left" width="63%">
Converts text host coordinates to screen coordinates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txcreatecaret">TxCreateCaret</a>
</td>
<td align="left" width="63%">
Creates a new shape for text host's caret.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txdeactivate">TxDeactivate</a>
</td>
<td align="left" width="63%">
Notifies the text host that the control is now inactive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txenablescrollbar">TxEnableScrollBar</a>
</td>
<td align="left" width="63%">
Enables or disables one or both scroll bar arrows in the text host window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txgetacceleratorpos">TxGetAcceleratorPos</a>
</td>
<td align="left" width="63%">
Requests the special character to use for the underlining accelerator character.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txgetbackstyle">TxGetBackStyle</a>
</td>
<td align="left" width="63%">
Requests the background style of the text host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txgetcharformat">TxGetCharFormat</a>
</td>
<td align="left" width="63%">
Requests the text host's default character format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txgetclientrect">TxGetClientRect</a>
</td>
<td align="left" width="63%">
Retrieves the client coordinates of the text host's client area.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txgetdc">TxGetDC</a>
</td>
<td align="left" width="63%">
Requests the device context for the text host window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txgetextent">TxGetExtent</a>
</td>
<td align="left" width="63%">
Requests the native size of the control in <b>HIMETRIC</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txgetmaxlength">TxGetMaxLength</a>
</td>
<td align="left" width="63%">
Gets the text host's maximum allowed length for the text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txgetparaformat">TxGetParaFormat</a>
</td>
<td align="left" width="63%">
Requests the text host's default paragraph format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txgetpasswordchar">TxGetPasswordChar</a>
</td>
<td align="left" width="63%">
Requests the text host's password character.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txgetpropertybits">TxGetPropertyBits</a>
</td>
<td align="left" width="63%">
Requests the bit property settings for the text host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txgetscrollbars">TxGetScrollBars</a>
</td>
<td align="left" width="63%">
Requests information about the scroll bars supported by the text host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txgetselectionbarwidth">TxGetSelectionBarWidth</a>
</td>
<td align="left" width="63%">
Gets the size of selection bar in <b>HIMETRIC</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txgetsyscolor">TxGetSysColor</a>
</td>
<td align="left" width="63%">
Gets the text host's color for a specified display element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txgetviewinset">TxGetViewInset</a>
</td>
<td align="left" width="63%">
Requests the dimensions of the white space inset around the text in the text host window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-tximmgetcontext">TxImmGetContext</a>
</td>
<td align="left" width="63%">
The 
			<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-tximmgetcontext">TxImmGetContext</a> method retrieves the IME input context associated with the text services host. 

This method is used only in Asian-language versions of the operating system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-tximmreleasecontext">TxImmReleaseContext</a>
</td>
<td align="left" width="63%">
Releases an input context returned by the <a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-tximmgetcontext">TxImmGetContext</a> method and unlocks the memory associated with the context. 

This method is used only in Asian-language versions of the operating system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txinvalidaterect">TxInvalidateRect</a>
</td>
<td align="left" width="63%">
Specifies a rectangle for the text host to add to the update region of the text host window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txkilltimer">TxKillTimer</a>
</td>
<td align="left" width="63%">
Requests the text host to destroy the specified timer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txnotify">TxNotify</a>
</td>
<td align="left" width="63%">
Notifies the text host of various events. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txreleasedc">TxReleaseDC</a>
</td>
<td align="left" width="63%">
Releases the device context obtained by the <a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txgetdc">TxGetDC</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txscreentoclient">TxScreenToClient</a>
</td>
<td align="left" width="63%">
Converts the screen coordinates to the text host window coordinates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txscrollwindowex">TxScrollWindowEx</a>
</td>
<td align="left" width="63%">
Requests the text host to scroll the content of the specified client area.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txsetcapture">TxSetCapture</a>
</td>
<td align="left" width="63%">
Sets the mouse capture in the text host's window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txsetcaretpos">TxSetCaretPos</a>
</td>
<td align="left" width="63%">
Moves the caret position to the specified coordinates in the text host window. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txsetcursor">TxSetCursor</a>
</td>
<td align="left" width="63%">
Establishes a new cursor shape (I-beam) in the text host's window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txsetfocus">TxSetFocus</a>
</td>
<td align="left" width="63%">
Sets the focus to the text host window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txsetscrollpos">TxSetScrollPos</a>
</td>
<td align="left" width="63%">
Requests that the text host set the position of the scroll box (thumb) in the specified scroll bar and, if requested, redraws the scroll bar to reflect the new position of the scroll box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txsetscrollrange">TxSetScrollRange</a>
</td>
<td align="left" width="63%">
Sets the minimum and maximum position values for the specified scroll bar in the text host window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txsettimer">TxSetTimer</a>
</td>
<td align="left" width="63%">
Requests that the text host create a timer with a specified time-out.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txshowcaret">TxShowCaret</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txshowcaret">TxShowCaret</a> method shows or hides the caret at the caret position in the text host window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txshowscrollbar">TxShowScrollBar</a>
</td>
<td align="left" width="63%">
Shows or hides the scroll bar in the text host window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-txviewchange">TxViewChange</a>
</td>
<td align="left" width="63%">
Indicates to the text host that the update region has changed.

</td>
</tr>
</table> 


## -remarks



You must implement the <b>ITextHost</b> interface before you call the <a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-createtextservices">CreateTextServices</a> function.

Applications do not call the <b>ITextHost</b> methods. A text services object created by the <a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-createtextservices">CreateTextServices</a> function calls the interface methods.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls Overview</a>
 

 

