---
UID: NN:vmr9.IVMRMixerControl9
title: IVMRMixerControl9 (vmr9.h)
description: The IVMRMixerControl9 interface enables an application to manipulate the incoming video streams on the Video Mixing Renderer Filter 9 (VMR-9). This interface is intended for use by applications only; it should not be used by upstream filters.
helpviewer_keywords: ["IVMRMixerControl9","IVMRMixerControl9 interface [DirectShow]","IVMRMixerControl9 interface [DirectShow]","described","IVMRMixerControl9Interface","dshow.ivmrmixercontrol9","vmr9/IVMRMixerControl9"]
old-location: dshow\ivmrmixercontrol9.htm
tech.root: dshow
ms.assetid: f311303a-8270-40b6-8153-e0bd8b232c69
ms.date: 12/05/2018
ms.keywords: IVMRMixerControl9, IVMRMixerControl9 interface [DirectShow], IVMRMixerControl9 interface [DirectShow],described, IVMRMixerControl9Interface, dshow.ivmrmixercontrol9, vmr9/IVMRMixerControl9
req.header: vmr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVMRMixerControl9
 - vmr9/IVMRMixerControl9
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRMixerControl9
---

# IVMRMixerControl9 interface


## -description

The <b>IVMRMixerControl9</b> interface enables an application to manipulate the incoming video streams on the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-9">Video Mixing Renderer Filter 9</a> (VMR-9). This interface is intended for use by applications only; it should not be used by upstream filters.

## -inheritance

The <b>IVMRMixerControl9</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRMixerControl9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -remarks

The VMR-9 supports this interface in mixing mode only. To enable mixing mode, call <a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrfilterconfig9-setnumberofstreams">IVMRFilterConfig9::SetNumberOfStreams</a>. Otherwise, <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> returns <b>E_NOINTERFACE</b>. 

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
