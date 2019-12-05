---
UID: NN:wmsbuffer.IWMSBufferAllocator
title: IWMSBufferAllocator (wmsbuffer.h)
description: The IWMSSBufferAllocator interface provides methods for allocating a buffer.
old-location: wmformat\iwmsbufferallocator.htm
tech.root: wmformat
ms.assetid: 021ced93-4b79-4821-a380-7fed43fd5391
ms.date: 12/05/2018
ms.keywords: IWMSBufferAllocator, IWMSBufferAllocator interface [windows Media Format], IWMSBufferAllocator interface [windows Media Format],described, IWMSBufferAllocatorInterface, wmformat.iwmsbufferallocator, wmsbuffer/IWMSBufferAllocator
ms.topic: interface
f1_keywords:
- wmsbuffer/IWMSBufferAllocator
dev_langs:
- c++
req.header: wmsbuffer.h
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
- wmsbuffer.h
api_name:
- IWMSBufferAllocator
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMSBufferAllocator interface


## -description



The <b>IWMSSBufferAllocator</b> interface provides methods for allocating a buffer. This method is implemented by the server object in Microsoft Windows Media Services 9 Series. For more information, see the Windows Media Services 9 Series SDK documentation.

<div class="alert"><b>Note</b>  This interface is available only on Windows Server 2003, Enterprise Edition, and Windows Server 2003, Datacenter Edition.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMSBufferAllocator</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMSBufferAllocator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMSBufferAllocator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsbuffer/nf-wmsbuffer-iwmsbufferallocator-allocatebuffer">AllocateBuffer</a>
</td>
<td align="left" width="63%">
Initializes a buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsbuffer/nf-wmsbuffer-iwmsbufferallocator-allocatepagesizebuffer">AllocatePageSizeBuffer</a>
</td>
<td align="left" width="63%">
Initializes a buffer that can be used to perform page-aligned reads.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>
 

 

