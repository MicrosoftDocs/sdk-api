---
UID: NL:textserv.ITextServices
title: ITextServices (textserv.h)
description: Extends the Text Object Model (TOM) to provide extra functionality for windowless operation.helpviewer_keywords: ["ITextServices","ITextServices interface [Windows Controls]","ITextServices interface [Windows Controls]","described","_win32_ITextServices","_win32_ITextServices_cpp","controls.ITextServices","controls._win32_ITextServices","textserv/ITextServices"]
old-location: controls\ITextServices.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itextservices.htm
ms.date: 12/05/2018
ms.keywords: ITextServices, ITextServices interface [Windows Controls], ITextServices interface [Windows Controls],described, _win32_ITextServices, _win32_ITextServices_cpp, controls.ITextServices, controls._win32_ITextServices, textserv/ITextServices
f1_keywords:
- textserv/ITextServices
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
- ITextServices
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextServices class


## -description


Extends the Text Object Model (TOM) to provide extra functionality for windowless operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextServices</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITextServices</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITextServices</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itextservices-ontxinplaceactivate">OnTxInPlaceActivate</a>
</td>
<td align="left" width="63%">
Notifies the text services object that this control is in-place active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itextservices-ontxinplacedeactivate">OnTxInPlaceDeactivate</a>
</td>
<td align="left" width="63%">
Notifies the text services object that this control is no longer in-place active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itextservices-ontxpropertybitschange">OnTxPropertyBitsChange</a>
</td>
<td align="left" width="63%">
Sets properties (represented by bits) for the control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itextservices-ontxsetcursor">OnTxSetCursor</a>
</td>
<td align="left" width="63%">
Notifies the text services object to set the cursor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itextservices-ontxuiactivate">OnTxUIActivate</a>
</td>
<td align="left" width="63%">
Notifies the text services object that the control is now UI active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itextservices-ontxuideactivate">OnTxUIDeactivate</a>
</td>
<td align="left" width="63%">
Notifies the text services object that the control is no longer UI active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itextservices-txdraw">TxDraw</a>
</td>
<td align="left" width="63%">
Draws the text services object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itextservices-txgetbaselinepos">TxGetBaseLinePos</a>
</td>
<td align="left" width="63%">
Gets the base line position of the first visible line, in pixels, relative to the text services client rectangle. This permits aligning controls on their base lines.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itextservices-txgetcachedsize">TxGetCachedSize</a>
</td>
<td align="left" width="63%">
Gets the cached drawing size (if any) that text services is using. Typically, this will be the size of the last client rectangle used in <a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itextservices-txdraw">TxDraw</a>, <a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itextservices-ontxsetcursor">OnTxSetCursor</a>, and so forth, although it is not guaranteed to be. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itextservices-txgetcurtargetx">TxGetCurTargetX</a>
</td>
<td align="left" width="63%">
Gets the target x position, that is, the current horizontal position of the caret.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itextservices-txgetdroptarget">TxGetDropTarget</a>
</td>
<td align="left" width="63%">
Gets the drop target for the text control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itextservices-txgethscroll">TxGetHScroll</a>
</td>
<td align="left" width="63%">
Gets the horizontal scroll bar information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itextservices-txgetnaturalsize">TxGetNaturalSize</a>
</td>
<td align="left" width="63%">
Enables a control to be resized so it fits its content appropriately.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itextservices-txgettext">TxGetText</a>
</td>
<td align="left" width="63%">
Gets all of the Unicode plain text in the control as a <b>BSTR</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itextservices-txgetvscroll">TxGetVScroll</a>
</td>
<td align="left" width="63%">
Gets vertical scroll bar state information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itextservices-txqueryhitpoint">TxQueryHitPoint</a>
</td>
<td align="left" width="63%">
Tests whether a specified point is within the rectangle of the text services object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itextservices-txsendmessage">TxSendMessage</a>
</td>
<td align="left" width="63%">
Used by the window host to forward messages sent from its window to the text services object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itextservices-txsettext">TxSetText</a>
</td>
<td align="left" width="63%">
Sets all of the text in the control.

</td>
</tr>
</table> 


## -remarks



In conjunction with the <a href="https://docs.microsoft.com/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a> interface, <b>ITextServices</b> provides the means by which a rich edit control can be used <i>without</i> creating a window.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Applications do not implement the <b>ITextServices</b> interface.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Applications can call the <a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-createtextservices">CreateTextServices</a> function to create a text services object. To retrieve an <b>ITextServices</b> pointer, call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the private <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer returned by <b>CreateTextServices</b>. You can then call the <b>ITextServices</b> methods to send messages to the text services object.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls Overview</a>
 

 

