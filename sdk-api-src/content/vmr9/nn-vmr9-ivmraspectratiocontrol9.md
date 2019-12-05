---
UID: NN:vmr9.IVMRAspectRatioControl9
title: IVMRAspectRatioControl9 (vmr9.h)
description: The IVMRAspectRatioControl9 interface controls whether the Video Mixing Renderer Filter 9 (VMR-9) preserves the aspect ratio of the source video.
old-location: dshow\ivmraspectratiocontrol9.htm
tech.root: DirectShow
ms.assetid: ae850eea-c283-4500-baa0-e26641576852
ms.date: 12/05/2018
ms.keywords: IVMRAspectRatioControl9, IVMRAspectRatioControl9 interface [DirectShow], IVMRAspectRatioControl9 interface [DirectShow],described, IVMRAspectRatioControl9Interface, dshow.ivmraspectratiocontrol9, vmr9/IVMRAspectRatioControl9
ms.topic: interface
f1_keywords:
- vmr9/IVMRAspectRatioControl9
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IVMRAspectRatioControl9
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRAspectRatioControl9 interface


## -description



The <code>IVMRAspectRatioControl9</code> interface controls whether the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/video-mixing-renderer-filter-9">Video Mixing Renderer Filter 9</a> (VMR-9) preserves the aspect ratio of the source video. This interface is available when the VMR is operating in either windowed or windowless modes. In windowless mode, the same functionality is provided by the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ivmrwindowlesscontrol">IVMRWindowlessControl</a> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRAspectRatioControl9</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRAspectRatioControl9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRAspectRatioControl9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmraspectratiocontrol9-getaspectratiomode">GetAspectRatioMode</a>
</td>
<td align="left" width="63%">
Queries whether the VMR will preserve the aspect ratio of the source video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmraspectratiocontrol9-setaspectratiomode">SetAspectRatioMode</a>
</td>
<td align="left" width="63%">
Specifies whether the VMR will preserve the aspect ratio of the source video.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

