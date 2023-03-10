---
UID: NF:wmsbuffer.IWMSBufferAllocator.AllocatePageSizeBuffer
title: IWMSBufferAllocator::AllocatePageSizeBuffer (wmsbuffer.h)
description: The AllocatePageSizeBuffer method initializes a buffer that can be used to perform page-aligned reads.
helpviewer_keywords: ["AllocatePageSizeBuffer","AllocatePageSizeBuffer method [windows Media Format]","AllocatePageSizeBuffer method [windows Media Format]","IWMSBufferAllocator interface","IWMSBufferAllocator interface [windows Media Format]","AllocatePageSizeBuffer method","IWMSBufferAllocator.AllocatePageSizeBuffer","IWMSBufferAllocator::AllocatePageSizeBuffer","IWMSBufferAllocatorAllocatePageSizeBuffer","wmformat.iwmsbufferallocator_allocatepagesizebuffer","wmsbuffer/IWMSBufferAllocator::AllocatePageSizeBuffer"]
old-location: wmformat\iwmsbufferallocator_allocatepagesizebuffer.htm
tech.root: wmformat
ms.assetid: 5d2340dd-8f91-4cce-840a-256c04329513
ms.date: 12/05/2018
ms.keywords: AllocatePageSizeBuffer, AllocatePageSizeBuffer method [windows Media Format], AllocatePageSizeBuffer method [windows Media Format],IWMSBufferAllocator interface, IWMSBufferAllocator interface [windows Media Format],AllocatePageSizeBuffer method, IWMSBufferAllocator.AllocatePageSizeBuffer, IWMSBufferAllocator::AllocatePageSizeBuffer, IWMSBufferAllocatorAllocatePageSizeBuffer, wmformat.iwmsbufferallocator_allocatepagesizebuffer, wmsbuffer/IWMSBufferAllocator::AllocatePageSizeBuffer
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
 - IWMSBufferAllocator::AllocatePageSizeBuffer
 - wmsbuffer/IWMSBufferAllocator::AllocatePageSizeBuffer
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
 - IWMSBufferAllocator.AllocatePageSizeBuffer
---

# IWMSBufferAllocator::AllocatePageSizeBuffer


## -description

The <b>AllocatePageSizeBuffer</b> method initializes a buffer that can be used to perform page-aligned reads.

## -parameters

### -param dwMaxBufferSize [in]

<b>DWORD</b> containing the size of the buffer in bytes.

### -param ppBuffer [out]

Address of a variable that receives a pointer to the <a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer</a> interface.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-iwmsbufferallocator">IWMSBufferAllocator Interface</a>