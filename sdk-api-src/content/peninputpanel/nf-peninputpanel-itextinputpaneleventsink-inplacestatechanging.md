---
UID: NF:peninputpanel.ITextInputPanelEventSink.InPlaceStateChanging
title: ITextInputPanelEventSink::InPlaceStateChanging
author: windows-driver-content
description: Occurs when the In-Place state is about to change.
old-location: tablet\itextinputpaneleventsink_inplacestatechanging.htm
old-project: tablet
ms.assetid: 866fcd8d-775c-4dc0-824f-6817767247d9
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: 866fcd8d-775c-4dc0-824f-6817767247d9, ITextInputPanelEventSink interface [Tablet PC],InPlaceStateChanging method, ITextInputPanelEventSink.InPlaceStateChanging, ITextInputPanelEventSink::InPlaceStateChanging, InPlaceStateChanging, InPlaceStateChanging method [Tablet PC], InPlaceStateChanging method [Tablet PC],ITextInputPanelEventSink interface, peninputpanel/ITextInputPanelEventSink::InPlaceStateChanging, tablet.itextinputpaneleventsink_inplacestatechanging
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
-	ITextInputPanelEventSink.InPlaceStateChanging
product: Windows
targetos: Windows
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ITextInputPanelEventSink::InPlaceStateChanging


## -description



Occurs when the In-Place state is about to change.




## -parameters




### -param oldInPlaceState [in]

The current state, as defined by the <a href="https://msdn.microsoft.com/95642cbf-4520-44cc-95ba-80de1fe3b447">InPlaceState Enumeration</a>.


### -param newInPlaceState [in]

The new state that the Input Panel is changing to, as defined by the <a href="https://msdn.microsoft.com/95642cbf-4520-44cc-95ba-80de1fe3b447">InPlaceState Enumeration</a>.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel Interface</a>



<a href="https://msdn.microsoft.com/e3ef6d65-ca6b-4587-bb21-3d3803a3432a">ITextInputPanelEventSink</a>



<a href="https://msdn.microsoft.com/bc01ecda-bb9f-40c6-8ac7-ffc4cc89b6a2">ITextInputPanelEventSink::InPlaceStateChanged Method</a>
 

 

