---
UID: NF:wmsbuffer.IWMSBufferAllocator.AllocateBuffer
title: IWMSBufferAllocator::AllocateBuffer (wmsbuffer.h)
description: The AllocateBuffer method initializes a buffer.
helpviewer_keywords: ["AllocateBuffer","AllocateBuffer method [windows Media Format]","AllocateBuffer method [windows Media Format]","IWMSBufferAllocator interface","IWMSBufferAllocator interface [windows Media Format]","AllocateBuffer method","IWMSBufferAllocator.AllocateBuffer","IWMSBufferAllocator::AllocateBuffer","IWMSBufferAllocatorAllocateBuffer","wmformat.iwmsbufferallocator_allocatebuffer","wmsbuffer/IWMSBufferAllocator::AllocateBuffer"]
old-location: wmformat\iwmsbufferallocator_allocatebuffer.htm
tech.root: wmformat
ms.assetid: 857fb8fa-0e86-46f2-907d-a244d6c699ef
ms.date: 12/05/2018
ms.keywords: AllocateBuffer, AllocateBuffer method [windows Media Format], AllocateBuffer method [windows Media Format],IWMSBufferAllocator interface, IWMSBufferAllocator interface [windows Media Format],AllocateBuffer method, IWMSBufferAllocator.AllocateBuffer, IWMSBufferAllocator::AllocateBuffer, IWMSBufferAllocatorAllocateBuffer, wmformat.iwmsbufferallocator_allocatebuffer, wmsbuffer/IWMSBufferAllocator::AllocateBuffer
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMSBufferAllocator::AllocateBuffer
 - wmsbuffer/IWMSBufferAllocator::AllocateBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmsbuffer.h
api_name:
 - IWMSBufferAllocator.AllocateBuffer
---

# IWMSBufferAllocator::AllocateBuffer


## -description

The <b>AllocateBuffer</b> method initializes a buffer.

## -parameters

### -param dwMaxBufferSize [in]

<b>DWORD</b> containing the maximum size of the buffer in bytes.

### -param ppBuffer [out]

Address of a variable that receives a pointer to the <a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer</a> interface.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-iwmsbufferallocator">IWMSBufferAllocator Interface</a>