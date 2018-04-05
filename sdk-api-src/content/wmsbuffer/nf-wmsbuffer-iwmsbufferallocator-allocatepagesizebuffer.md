---
UID: NF:wmsbuffer.IWMSBufferAllocator.AllocatePageSizeBuffer
title: IWMSBufferAllocator::AllocatePageSizeBuffer method
author: windows-driver-content
description: The AllocatePageSizeBuffer method initializes a buffer that can be used to perform page-aligned reads.
old-location: wmformat\iwmsbufferallocator_allocatepagesizebuffer.htm
old-project: wmformat
ms.assetid: 5d2340dd-8f91-4cce-840a-256c04329513
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: AllocatePageSizeBuffer method [windows Media Format], AllocatePageSizeBuffer method [windows Media Format], IWMSBufferAllocator interface, AllocatePageSizeBuffer,IWMSBufferAllocator.AllocatePageSizeBuffer, IWMSBufferAllocator, IWMSBufferAllocator interface [windows Media Format], AllocatePageSizeBuffer method, IWMSBufferAllocator::AllocatePageSizeBuffer, IWMSBufferAllocatorAllocatePageSizeBuffer, wmformat.iwmsbufferallocator_allocatepagesizebuffer, wmsbuffer/IWMSBufferAllocator::AllocatePageSizeBuffer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmsbuffer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Format 9 Series SDK, or later versions of the SDK
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
-	Wmsbuffer.h
api_name:
-	IWMSBufferAllocator.AllocatePageSizeBuffer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMSBufferAllocator::AllocatePageSizeBuffer method


## -description



The <b>AllocatePageSizeBuffer</b> method initializes a buffer that can be used to perform page-aligned reads.




## -parameters




### -param dwMaxBufferSize [in]

<b>DWORD</b> containing the size of the buffer in bytes.


### -param ppBuffer [out]

Address of a variable that receives a pointer to the <a href="https://msdn.microsoft.com/c47c016a-e7eb-4a2c-b365-5537749db5bc">INSSBuffer</a> interface.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/021ced93-4b79-4821-a380-7fed43fd5391">IWMSBufferAllocator Interface</a>
 

 

