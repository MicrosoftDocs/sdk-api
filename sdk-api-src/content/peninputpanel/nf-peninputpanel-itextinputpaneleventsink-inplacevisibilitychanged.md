---
UID: NF:peninputpanel.ITextInputPanelEventSink.InPlaceVisibilityChanged
title: ITextInputPanelEventSink::InPlaceVisibilityChanged
author: windows-driver-content
description: Occurs when the Tablet PC Input Panel has switched between visible and invisible.
old-location: tablet\itextinputpaneleventsink_inplacevisibilitychanged.htm
old-project: tablet
ms.assetid: 7ec8acd4-fbb9-4801-880b-fe0d5d3fa3c2
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: 7ec8acd4-fbb9-4801-880b-fe0d5d3fa3c2, ITextInputPanelEventSink interface [Tablet PC],InPlaceVisibilityChanged method, ITextInputPanelEventSink.InPlaceVisibilityChanged, ITextInputPanelEventSink::InPlaceVisibilityChanged, InPlaceVisibilityChanged, InPlaceVisibilityChanged method [Tablet PC], InPlaceVisibilityChanged method [Tablet PC],ITextInputPanelEventSink interface, peninputpanel/ITextInputPanelEventSink::InPlaceVisibilityChanged, tablet.itextinputpaneleventsink_inplacevisibilitychanged
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
-	ITextInputPanelEventSink.InPlaceVisibilityChanged
product: Windows
targetos: Windows
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ITextInputPanelEventSink::InPlaceVisibilityChanged


## -description



Occurs when the Tablet PC Input Panel has switched between visible and invisible.




## -parameters




### -param oldVisible [in]

<b>TRUE</b> if the Input Panel has changed from visible to invisible, otherwise <b>FALSE</b>.


### -param newVisible [in]

<b>TRUE</b> if the Input Panel has changed from invisible to visible, otherwise <b>FALSE</b>.


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



<a href="https://msdn.microsoft.com/957e1c24-3eee-4a6f-9157-961e3d6914b7">ITextInputPanelEventSink::InPlaceVisibilityChanging Method</a>
 

 

