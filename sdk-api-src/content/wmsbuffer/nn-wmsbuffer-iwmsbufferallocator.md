---
UID: NN:wmsbuffer.IWMSBufferAllocator
title: IWMSBufferAllocator
author: windows-sdk-content
description: The IWMSSBufferAllocator interface provides methods for allocating a buffer.
old-location: wmformat\iwmsbufferallocator.htm
old-project: wmformat
ms.assetid: 021ced93-4b79-4821-a380-7fed43fd5391
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWMSBufferAllocator, IWMSBufferAllocator interface [windows Media Format], IWMSBufferAllocator interface [windows Media Format],described, IWMSBufferAllocatorInterface, wmformat.iwmsbufferallocator, wmsbuffer/IWMSBufferAllocator
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
req.typenames: WMPServices_StreamState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmsbuffer.h
api_name:
-	IWMSBufferAllocator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMSBufferAllocator interface


## -description



The <b>IWMSSBufferAllocator</b> interface provides methods for allocating a buffer. This method is implemented by the server object in Microsoft Windows Media Services 9 Series. For more information, see the Windows Media Services 9 Series SDK documentation.

<div class="alert"><b>Note</b>  This interface is available only on Windows Server 2003, Enterprise Edition, and Windows Server 2003, Datacenter Edition.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMSBufferAllocator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMSBufferAllocator</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/857fb8fa-0e86-46f2-907d-a244d6c699ef">AllocateBuffer</a>
</td>
<td align="left" width="63%">
Initializes a buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d2340dd-8f91-4cce-840a-256c04329513">AllocatePageSizeBuffer</a>
</td>
<td align="left" width="63%">
Initializes a buffer that can be used to perform page-aligned reads.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

