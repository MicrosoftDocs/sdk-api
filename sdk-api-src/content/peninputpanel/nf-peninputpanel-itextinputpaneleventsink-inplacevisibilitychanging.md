---
UID: NF:peninputpanel.ITextInputPanelEventSink.InPlaceVisibilityChanging
title: ITextInputPanelEventSink::InPlaceVisibilityChanging
author: windows-sdk-content
description: Occurs when the Tablet PC Input Panel is about to switch between visible and invisible.
old-location: tablet\itextinputpaneleventsink_inplacevisibilitychanging.htm
old-project: tablet
ms.assetid: 957e1c24-3eee-4a6f-9157-961e3d6914b7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 957e1c24-3eee-4a6f-9157-961e3d6914b7, ITextInputPanelEventSink interface [Tablet PC],InPlaceVisibilityChanging method, ITextInputPanelEventSink.InPlaceVisibilityChanging, ITextInputPanelEventSink::InPlaceVisibilityChanging, InPlaceVisibilityChanging, InPlaceVisibilityChanging method [Tablet PC], InPlaceVisibilityChanging method [Tablet PC],ITextInputPanelEventSink interface, peninputpanel/ITextInputPanelEventSink::InPlaceVisibilityChanging, tablet.itextinputpaneleventsink_inplacevisibilitychanging
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: EventMask
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tiptsf.dll
api_name:
 - ITextInputPanelEventSink.InPlaceVisibilityChanging
product: Windows
targetos: Windows
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
req.product: ADAM
---

# ITextInputPanelEventSink::InPlaceVisibilityChanging


## -description



Occurs when the Tablet PC Input Panel is about to switch between visible and invisible.




## -parameters




### -param oldVisible [in]

<b>TRUE</b> if the Input Panel is changing from visible to invisible, otherwise <b>FALSE</b>.


### -param newVisible [in]

<b>TRUE</b> if the Input Panel is changing from invisible to visible, otherwise <b>FALSE</b>.


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



<a href="https://msdn.microsoft.com/7ec8acd4-fbb9-4801-880b-fe0d5d3fa3c2">ITextInputPanelEventSink::InPlaceVisibilityChanged Method</a>
 

 

