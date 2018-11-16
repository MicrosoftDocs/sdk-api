---
UID: NN:wmsdkidl.IWMWriterPostViewCallback
title: IWMWriterPostViewCallback
author: windows-sdk-content
description: The IWMWriterPostViewCallback interface manages the receiving of uncompressed samples from the writer. Postview can be used only for video streams.This interface must be implemented by the application and passed to IWMWriterPostView::SetPostViewCallback.
old-location: wmformat\iwmwriterpostviewcallback.htm
tech.root: wmformat
ms.assetid: 987dd3b4-2245-4640-820c-5a9660ab5e37
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWMWriterPostViewCallback, IWMWriterPostViewCallback interface [windows Media Format], IWMWriterPostViewCallback interface [windows Media Format],described, IWMWriterPostViewCallbackInterface, wmformat.iwmwriterpostviewcallback, wmsdkidl/IWMWriterPostViewCallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMWriterPostViewCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMWriterPostViewCallback interface


## -description



The <b>IWMWriterPostViewCallback</b> interface manages the receiving of uncompressed samples from the writer. Postview can be used only for video streams.

This interface must be implemented by the application and passed to <a href="https://msdn.microsoft.com/c2814f32-1787-44a6-8ffc-5d2a9aca8601">IWMWriterPostView::SetPostViewCallback</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMWriterPostViewCallback</b> interface inherits from <a href="https://msdn.microsoft.com/a8d8eed8-0a87-40ce-b1bf-2d476c2e4ae3">IWMStatusCallback</a>. <b>IWMWriterPostViewCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMWriterPostViewCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e48132c4-b222-4401-99b3-7906c0df4ec1">AllocateForPostView</a>
</td>
<td align="left" width="63%">
Allocates a buffer for use in postviewing operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d29a746-70fe-495e-a7f2-dbf085829496">OnPostViewSample</a>
</td>
<td align="left" width="63%">
Called when new postview data is available.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/a8d8eed8-0a87-40ce-b1bf-2d476c2e4ae3">IWMStatusCallback Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/9da3c749-f6bd-43b5-9eff-3a637ddef048">To Use Writer Postview</a>



<a href="https://msdn.microsoft.com/8058b7fe-7d02-4572-ad43-6867d4ceb7e9">Writer Object</a>
 

 

