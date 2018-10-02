---
UID: NN:wmsdkidl.IWMReaderAllocatorEx
title: IWMReaderAllocatorEx
author: windows-sdk-content
description: The IWMReaderAllocatorEx interface provides expanded alternatives to the AllocateForOutput and AllocateForStream methods of the IWMReaderCallbackAdvanced interface.
old-location: wmformat\iwmreaderallocatorex.htm
tech.root: wmformat
ms.assetid: be727c7b-b252-44db-825b-5c683e551fd2
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMReaderAllocatorEx, IWMReaderAllocatorEx interface [windows Media Format], IWMReaderAllocatorEx interface [windows Media Format],described, IWMReaderAllocatorExInterface, wmformat.iwmreaderallocatorex, wmsdkidl/IWMReaderAllocatorEx
ms.prod: windows
ms.technology: windows-sdk
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
 - IWMReaderAllocatorEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReaderAllocatorEx interface


## -description



The <b>IWMReaderAllocatorEx</b> interface provides expanded alternatives to the <a href="https://msdn.microsoft.com/bd7340c9-9380-4dba-b8ac-2a616ce9949f">AllocateForOutput</a> and <a href="https://msdn.microsoft.com/82d31f4b-d8a8-4538-be5e-dd9149e3f420">AllocateForStream</a> methods of the <a href="https://msdn.microsoft.com/9d18961a-5ea4-4f3e-b473-7399e155f800">IWMReaderCallbackAdvanced</a> interface. This interface is implemented by the application, which passes this interface pointer to the synchronous reader object by calling <a href="https://msdn.microsoft.com/ed94977e-e930-4045-a69d-36109e7e21c9">IWMSyncReader2::SetAllocateForStream</a> or <a href="https://msdn.microsoft.com/2f0c754e-f09c-472f-8f40-3fcd0fb29c48">SetAllocateForOutput</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMReaderAllocatorEx</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMReaderAllocatorEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMReaderAllocatorEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2e4881b-2186-47c9-b74e-3a59a9fac7c9">AllocateForOutputEx</a>
</td>
<td align="left" width="63%">
Allocates a buffer for samples delivered to the <a href="https://msdn.microsoft.com/0f6e4d4f-4295-44ff-95bc-e683bdbab8e0">IWMReaderCallback::OnSample</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb12f0e1-dc9c-447e-a28d-30c45eb95d09">AllocateForStreamEx</a>
</td>
<td align="left" width="63%">
Allocates a buffer for samples delivered to the <a href="https://msdn.microsoft.com/6bfdd903-a3a4-4ef4-b88a-4d24c9c0f4b8">IWMReaderCallbackAdvanced::OnStreamSample</a> method.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/da66ef5b-ec92-445c-90ba-5ee89e0def36">Allocating Buffers for File Reading</a>



<a href="https://msdn.microsoft.com/a7a20f87-6f21-4fe8-8889-1b6689daf833">IWMReaderAdvanced Interface</a>



<a href="https://msdn.microsoft.com/69b897a8-cc26-445d-9d41-b917b399fb14">IWMReaderCallback Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>
 

 

