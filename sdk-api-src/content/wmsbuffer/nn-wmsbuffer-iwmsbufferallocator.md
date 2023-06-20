---
UID: NN:wmsbuffer.IWMSBufferAllocator
title: IWMSBufferAllocator (wmsbuffer.h)
description: The IWMSSBufferAllocator interface provides methods for allocating a buffer.
helpviewer_keywords: ["IWMSBufferAllocator","IWMSBufferAllocator interface [windows Media Format]","IWMSBufferAllocator interface [windows Media Format]","described","IWMSBufferAllocatorInterface","wmformat.iwmsbufferallocator","wmsbuffer/IWMSBufferAllocator"]
old-location: wmformat\iwmsbufferallocator.htm
tech.root: wmformat
ms.assetid: 021ced93-4b79-4821-a380-7fed43fd5391
ms.date: 4/26/2023
ms.keywords: IWMSBufferAllocator, IWMSBufferAllocator interface [windows Media Format], IWMSBufferAllocator interface [windows Media Format],described, IWMSBufferAllocatorInterface, wmformat.iwmsbufferallocator, wmsbuffer/IWMSBufferAllocator
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMSBufferAllocator
 - wmsbuffer/IWMSBufferAllocator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsbuffer.h
api_name:
 - IWMSBufferAllocator
---

# IWMSBufferAllocator interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMSSBufferAllocator</b> interface provides methods for allocating a buffer. This method is implemented by the server object in Microsoft Windows Media Services 9 Series. For more information, see the Windows Media Services 9 Series SDK documentation.

<div class="alert"><b>Note</b>  This interface is available only on Windows Server 2003, Enterprise Edition, and Windows Server 2003, Datacenter Edition.</div>
<div> </div>

## -inheritance

The <b>IWMSBufferAllocator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMSBufferAllocator</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>
