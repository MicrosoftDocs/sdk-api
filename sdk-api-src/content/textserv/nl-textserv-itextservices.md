---
UID: NL:textserv.ITextServices
title: ITextServices
author: windows-sdk-content
description: Extends the Text Object Model (TOM) to provide extra functionality for windowless operation.
old-location: controls\ITextServices.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itextservices.htm
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: ITextServices, ITextServices interface [Windows Controls], ITextServices interface [Windows Controls],described, _win32_ITextServices, _win32_ITextServices_cpp, controls.ITextServices, controls._win32_ITextServices, textserv/ITextServices
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
req.typenames: TMGR_DIRECTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextServices
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextServices class


## -description


Extends the Text Object Model (TOM) to provide extra functionality for windowless operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextServices</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITextServices</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/80e003fd-802a-49dd-9616-b4cc7b77fd09">OnTxInPlaceActivate</a>
</td>
<td align="left" width="63%">
Notifies the text services object that this control is in-place active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed07023b-abe2-4f2d-994d-3d3c2df5c80e">OnTxInPlaceDeactivate</a>
</td>
<td align="left" width="63%">
Notifies the text services object that this control is no longer in-place active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/41ae1a84-e721-4666-bac0-eb11c9b55279">OnTxPropertyBitsChange</a>
</td>
<td align="left" width="63%">
Sets properties (represented by bits) for the control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9656a2ed-bd66-4083-a2b4-c6255f136f9d">OnTxSetCursor</a>
</td>
<td align="left" width="63%">
Notifies the text services object to set the cursor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0bcaa1dc-36fd-48e0-993d-f5e629a54b0e">OnTxUIActivate</a>
</td>
<td align="left" width="63%">
Notifies the text services object that the control is now UI active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f44bc87-c87b-4536-aadc-dc93463247c7">OnTxUIDeactivate</a>
</td>
<td align="left" width="63%">
Notifies the text services object that the control is no longer UI active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5fb14a41-2e73-4760-ba77-f1bfd2a1184b">TxDraw</a>
</td>
<td align="left" width="63%">
Draws the text services object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/445c66d2-63b8-4d38-bb98-e966a360382f">TxGetBaseLinePos</a>
</td>
<td align="left" width="63%">
Gets the base line position of the first visible line, in pixels, relative to the text services client rectangle. This permits aligning controls on their base lines.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/67ceeaed-3c27-4ff2-bfff-83ad45b70863">TxGetCachedSize</a>
</td>
<td align="left" width="63%">
Gets the cached drawing size (if any) that text services is using. Typically, this will be the size of the last client rectangle used in <a href="https://msdn.microsoft.com/5fb14a41-2e73-4760-ba77-f1bfd2a1184b">TxDraw</a>, <a href="https://msdn.microsoft.com/9656a2ed-bd66-4083-a2b4-c6255f136f9d">OnTxSetCursor</a>, and so forth, although it is not guaranteed to be. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ad9ce01-8fd0-403d-99f3-5236f0d26203">TxGetCurTargetX</a>
</td>
<td align="left" width="63%">
Gets the target x position, that is, the current horizontal position of the caret.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b266ff4-8e7e-4917-8744-1a73fe901713">TxGetDropTarget</a>
</td>
<td align="left" width="63%">
Gets the drop target for the text control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/490cd2aa-a5ae-44da-8c6e-052954930f5c">TxGetHScroll</a>
</td>
<td align="left" width="63%">
Gets the horizontal scroll bar information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66798915-af6f-4a18-813b-872bf0298824">TxGetNaturalSize</a>
</td>
<td align="left" width="63%">
Enables a control to be resized so it fits its content appropriately.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5056cd1-4fca-40ee-8a69-1940c46e3f86">TxGetText</a>
</td>
<td align="left" width="63%">
Gets all of the Unicode plain text in the control as a <b>BSTR</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ff83535-10fd-42cb-93bd-b3bf142d8b49">TxGetVScroll</a>
</td>
<td align="left" width="63%">
Gets vertical scroll bar state information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/926bab0d-667f-40bf-b48d-9e352be41960">TxQueryHitPoint</a>
</td>
<td align="left" width="63%">
Tests whether a specified point is within the rectangle of the text services object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86e64047-68f7-4cd8-a18d-0f2e84340f52">TxSendMessage</a>
</td>
<td align="left" width="63%">
Used by the window host to forward messages sent from its window to the text services object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29be3eba-285c-4297-b692-0a5fcb4797c6">TxSetText</a>
</td>
<td align="left" width="63%">
Sets all of the text in the control.

</td>
</tr>
</table> 


## -remarks



In conjunction with the <a href="https://msdn.microsoft.com/28d86b94-2d36-4749-8954-3857bf6dbdac">ITextHost</a> interface, <b>ITextServices</b> provides the means by which a rich edit control can be used <i>without</i> creating a window.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Applications do not implement the <b>ITextServices</b> interface.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Applications can call the <a href="https://msdn.microsoft.com/475ede7d-75ba-4eda-8253-1166fc9f45fe">CreateTextServices</a> function to create a text services object. To retrieve an <b>ITextServices</b> pointer, call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on the private <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointer returned by <b>CreateTextServices</b>. You can then call the <b>ITextServices</b> methods to send messages to the text services object.




## -see-also




<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls Overview</a>
 

 

