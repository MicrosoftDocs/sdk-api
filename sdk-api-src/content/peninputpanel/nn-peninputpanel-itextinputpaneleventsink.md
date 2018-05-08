---
UID: NN:peninputpanel.ITextInputPanelEventSink
title: ITextInputPanelEventSink
author: windows-driver-content
description: Defines methods that handle the ITextInputPanel Interface events.
old-location: tablet\itextinputpaneleventsink.htm
old-project: tablet
ms.assetid: e3ef6d65-ca6b-4587-bb21-3d3803a3432a
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: ITextInputPanelEventSink, ITextInputPanelEventSink interface [Tablet PC], ITextInputPanelEventSink interface [Tablet PC],described, e3ef6d65-ca6b-4587-bb21-3d3803a3432a, peninputpanel/ITextInputPanelEventSink, tablet.itextinputpaneleventsink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: peninputpanel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: EventMask
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tiptsf.dll
api_name:
-	ITextInputPanelEventSink
product: Windows
targetos: Windows
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ITextInputPanelEventSink interface


## -description



Defines methods that handle the <a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel Interface</a> events.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextInputPanelEventSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITextInputPanelEventSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITextInputPanelEventSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70c4dca4-274f-40ae-b71a-f86a2e8fbd3d">CorrectionModeChanged</a>
</td>
<td align="left" width="63%">
Occurs when the correction comb on the Tablet PC Input Panel has changed modes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f20b77dc-a04f-4bd3-9aa0-3a0c3d98e4a8">CorrectionModeChanging</a>
</td>
<td align="left" width="63%">
Occurs when the correction comb on the Tablet PC Input Panel is about to change modes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd1f7cba-0a0f-49da-ad67-5c2e01830750">InPlaceSizeChanged</a>
</td>
<td align="left" width="63%">
Occurs when the In-Place Input Panel size has changed due to a user resize, auto growth, or an input area change.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af9998a0-42ab-410d-980e-59a765d44667">InPlaceSizeChanging</a>
</td>
<td align="left" width="63%">
Occurs when the In-Place Input Panel size is about to change due to a user resize, auto growth, or an input area change.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc01ecda-bb9f-40c6-8ac7-ffc4cc89b6a2">InPlaceStateChanged</a>
</td>
<td align="left" width="63%">
Occurs when the In-Place state has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/866fcd8d-775c-4dc0-824f-6817767247d9">InPlaceStateChanging</a>
</td>
<td align="left" width="63%">
Occurs when the In-Place state is about to change.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ec8acd4-fbb9-4801-880b-fe0d5d3fa3c2">InPlaceVisibilityChanged</a>
</td>
<td align="left" width="63%">
Occurs when the Tablet PC Input Panel has switched between visible and invisible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/957e1c24-3eee-4a6f-9157-961e3d6914b7">InPlaceVisibilityChanging</a>
</td>
<td align="left" width="63%">
Occurs when the Tablet PC Input Panel is about to switch between visible and invisible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b30eaa39-a1f7-4c50-992f-11030bb175f9">InputAreaChanged</a>
</td>
<td align="left" width="63%">
Occurs when the input area has changed on the Tablet PC Input Panel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5f96798-2428-4acd-9d9a-addfdf14bb84">InputAreaChanging</a>
</td>
<td align="left" width="63%">
Occurs when the input area is about to change on the Tablet PC Input Panel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61f3c21f-8658-421b-8494-d39a2faacc66">TextInserted</a>
</td>
<td align="left" width="63%">
Occurs when the Tablet PC Input Panel has inserted text into the control with input focus. Provides access to the ink the user entered in the Input Panel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e2ca5e2-a407-44cd-b489-c118401ca21b">TextInserting</a>
</td>
<td align="left" width="63%">
Occurs when the Tablet PC Input Panel is about to insert text into the control with input focus. Provides access to the ink the user entered in the Input Panel.

</td>
</tr>
</table> 


## -remarks



This element is declared in Peninputpanel.h.




## -see-also




<a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel Interface</a>
 

 

