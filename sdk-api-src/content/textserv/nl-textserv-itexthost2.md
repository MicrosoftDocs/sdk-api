---
UID: NL:textserv.ITextHost2
title: ITextHost2 (textserv.h)
description: The ITextHost2 interface extends the ITextHost interface.helpviewer_keywords: ["ITextHost2","ITextHost2 interface [Windows Controls]","ITextHost2 interface [Windows Controls]","described","controls.itexthost2","textserv/ITextHost2"]
old-location: controls\itexthost2.htm
tech.root: Controls
ms.assetid: A715E70C-E8BB-4796-BDA6-90B745EC7761
ms.date: 12/05/2018
ms.keywords: ITextHost2, ITextHost2 interface [Windows Controls], ITextHost2 interface [Windows Controls],described, controls.itexthost2, textserv/ITextHost2
f1_keywords:
- textserv/ITextHost2
dev_langs:
- c++
req.header: textserv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
- ITextHost2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextHost2 class


## -description


The <b>ITextHost2</b> interface extends the <a href="https://docs.microsoft.com/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a> interface. The purpose of these interfaces, along with <a href="https://docs.microsoft.com/windows/desktop/api/textserv/nl-textserv-itextservices">ITextServices</a> and <a href="https://docs.microsoft.com/windows/desktop/api/textserv/nl-textserv-itextservices2">ITextServices2</a>, is to enable rich edit controls to run without a dedicated window. The rich edit client typically has a window (<b>HWND</b>) that it shares with a number of windowless controls. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextHost2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>. <b>ITextHost2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITextHost2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost2-txdestroycaret">TxDestroyCaret</a>
</td>
<td align="left" width="63%">
Destroys the caret (Direct2D only).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost2-txfreetextservicesnotification">TxFreeTextServicesNotification</a>
</td>
<td align="left" width="63%">
Notifies the text host that text services have been freed. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost2-txgeteastasianflags">TxGetEastAsianFlags</a>
</td>
<td align="left" width="63%">
Gets whether IME input is allowed and whether the edit styles include <a href="https://docs.microsoft.com/windows/desktop/Controls/rich-edit-control-styles">ES_SELFIME</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost2-txgeteditstyle">TxGetEditStyle</a>
</td>
<td align="left" width="63%">
Gets whether a rich edit control is in a dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost2-txgethorzextent">TxGetHorzExtent</a>
</td>
<td align="left" width="63%">
Gets the horizontal scroll extent of the text host window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost2-txgetpalette">TxGetPalette</a>
</td>
<td align="left" width="63%">
Retrieves the color palette of the rich edit control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost2-txgetwindow">TxGetWindow</a>
</td>
<td align="left" width="63%">
Retrieves the handle of the text host window for the rich edit control. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost2-txgetwindowstyles">TxGetWindowStyles</a>
</td>
<td align="left" width="63%">
Retrieves the window styles and extended windows styles of the text host window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost2-txisdoubleclickpending">TxIsDoubleClickPending</a>
</td>
<td align="left" width="63%">
Discovers whether the message queue contains a <a href="https://docs.microsoft.com/windows/desktop/inputdev/wm-lbuttondblclk">WM_LBUTTONDBLCLK</a>  message that is pending for the text host window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost2-txsetcursor2">TxSetCursor2</a>
</td>
<td align="left" width="63%">
Sets the shape of the cursor in the text host window. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost2-txsetforegroundwindow">TxSetForegroundWindow</a>
</td>
<td align="left" width="63%">
Sets the rich edit control's host window as the foreground window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost2-txshowdropcaret">TxShowDropCaret</a>
</td>
<td align="left" width="63%">
Shows or hides the  caret during the drop portion of a drag-and-drop operation (Direct2D only).

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>
 

 

