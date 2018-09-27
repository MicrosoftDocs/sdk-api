---
UID: NL:textserv.ITextHost2
title: ITextHost2
author: windows-sdk-content
description: The ITextHost2 interface extends the ITextHost interface.
old-location: controls\itexthost2.htm
tech.root: Controls
ms.assetid: A715E70C-E8BB-4796-BDA6-90B745EC7761
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ITextHost2, ITextHost2 interface [Windows Controls], ITextHost2 interface [Windows Controls],described, controls.itexthost2, textserv/ITextHost2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextHost2 class


## -description


The <b>ITextHost2</b> interface extends the <a href="https://msdn.microsoft.com/en-us/library/Bb787615(v=VS.85).aspx">ITextHost</a> interface. The purpose of these interfaces, along with <a href="https://msdn.microsoft.com/en-us/library/Bb787617(v=VS.85).aspx">ITextServices</a> and <a href="https://msdn.microsoft.com/B5DC90BA-F9A5-45DC-8C8A-784380C38769">ITextServices2</a>, is to enable rich edit controls to run without a dedicated window. The rich edit client typically has a window (<b>HWND</b>) that it shares with a number of windowless controls. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextHost2</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Bb787615(v=VS.85).aspx">ITextHost</a>. <b>ITextHost2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/627FEF54-FD74-4A41-89FC-E02EBD29D18A">TxDestroyCaret</a>
</td>
<td align="left" width="63%">
Destroys the caret (Direct2D only).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AD017B2A-C38E-4A55-AA31-84639BE87FA8">TxFreeTextServicesNotification</a>
</td>
<td align="left" width="63%">
Notifies the text host that text services have been freed. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3D704159-795A-4BD6-B699-EC311D9B780C">TxGetEastAsianFlags</a>
</td>
<td align="left" width="63%">
Gets whether IME input is allowed and whether the edit styles include <a href="https://msdn.microsoft.com/en-us/library/Bb774367(v=VS.85).aspx">ES_SELFIME</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8C5468C9-D152-4F57-9E8A-23B4852BFD69">TxGetEditStyle</a>
</td>
<td align="left" width="63%">
Gets whether a rich edit control is in a dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86D53FEF-DB50-41F6-AC99-106FC01BCD61">TxGetHorzExtent</a>
</td>
<td align="left" width="63%">
Gets the horizontal scroll extent of the text host window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A9881BE7-0434-40EF-9BD8-AB8EF4E31582">TxGetPalette</a>
</td>
<td align="left" width="63%">
Retrieves the color palette of the rich edit control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42594B92-298B-4659-87EC-D10C6996CECF">TxGetWindow</a>
</td>
<td align="left" width="63%">
Retrieves the handle of the text host window for the rich edit control. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51885B3E-3DEE-461C-8625-3DE9D8C1F992">TxGetWindowStyles</a>
</td>
<td align="left" width="63%">
Retrieves the window styles and extended windows styles of the text host window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24051A4F-70CD-4147-B623-BC818F3F9AF2">TxIsDoubleClickPending</a>
</td>
<td align="left" width="63%">
Discovers whether the message queue contains a <a href="https://msdn.microsoft.com/en-us/library/ms645606(v=VS.85).aspx">WM_LBUTTONDBLCLK</a>  message that is pending for the text host window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9671AEEC-CA31-4CE7-8B40-57859E36EF23">TxSetCursor2</a>
</td>
<td align="left" width="63%">
Sets the shape of the cursor in the text host window. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0C3400BB-FC9A-43C3-92B4-055DE0A17717">TxSetForegroundWindow</a>
</td>
<td align="left" width="63%">
Sets the rich edit control's host window as the foreground window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D7FAD45E-3467-4F07-A0D9-3131E48C314B">TxShowDropCaret</a>
</td>
<td align="left" width="63%">
Shows or hides the  caret during the drop portion of a drag-and-drop operation (Direct2D only).

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb787615(v=VS.85).aspx">ITextHost</a>
 

 

