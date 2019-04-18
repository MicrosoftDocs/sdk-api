---
UID: NN:wmsdkidl.IWMReaderAllocatorEx
title: IWMReaderAllocatorEx (wmsdkidl.h)
author: windows-sdk-content
description: The IWMReaderAllocatorEx interface provides expanded alternatives to the AllocateForOutput and AllocateForStream methods of the IWMReaderCallbackAdvanced interface.
old-location: wmformat\iwmreaderallocatorex.htm
tech.root: wmformat
ms.assetid: be727c7b-b252-44db-825b-5c683e551fd2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMReaderAllocatorEx, IWMReaderAllocatorEx interface [windows Media Format], IWMReaderAllocatorEx interface [windows Media Format],described, IWMReaderAllocatorExInterface, wmformat.iwmreaderallocatorex, wmsdkidl/IWMReaderAllocatorEx
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
ms.custom: 19H1
---

# IWMReaderAllocatorEx interface


## -description



The <b>IWMReaderAllocatorEx</b> interface provides expanded alternatives to the <a href="https://msdn.microsoft.com/en-us/library/Dd743495(v=VS.85).aspx">AllocateForOutput</a> and <a href="https://msdn.microsoft.com/en-us/library/Dd743496(v=VS.85).aspx">AllocateForStream</a> methods of the <a href="https://msdn.microsoft.com/en-us/library/Dd743494(v=VS.85).aspx">IWMReaderCallbackAdvanced</a> interface. This interface is implemented by the application, which passes this interface pointer to the synchronous reader object by calling <a href="https://msdn.microsoft.com/en-us/library/Dd798581(v=VS.85).aspx">IWMSyncReader2::SetAllocateForStream</a> or <a href="https://msdn.microsoft.com/en-us/library/Dd798580(v=VS.85).aspx">SetAllocateForOutput</a>.




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
<a href="https://msdn.microsoft.com/en-us/library/Dd743491(v=VS.85).aspx">AllocateForOutputEx</a>
</td>
<td align="left" width="63%">
Allocates a buffer for samples delivered to the <a href="https://msdn.microsoft.com/en-us/library/Dd743503(v=VS.85).aspx">IWMReaderCallback::OnSample</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743492(v=VS.85).aspx">AllocateForStreamEx</a>
</td>
<td align="left" width="63%">
Allocates a buffer for samples delivered to the <a href="https://msdn.microsoft.com/en-us/library/Dd743500(v=VS.85).aspx">IWMReaderCallbackAdvanced::OnStreamSample</a> method.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/da66ef5b-ec92-445c-90ba-5ee89e0def36">Allocating Buffers for File Reading</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757429(v=VS.85).aspx">IWMReaderAdvanced Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743493(v=VS.85).aspx">IWMReaderCallback Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>
 

 

