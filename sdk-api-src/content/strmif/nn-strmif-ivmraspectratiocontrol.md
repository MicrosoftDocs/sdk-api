---
UID: NN:strmif.IVMRAspectRatioControl
title: IVMRAspectRatioControl (strmif.h)
description: The IVMRAspectRatioControl interface controls whether the Video Mixing Renderer Filter 7 (VMR-7) preserves the aspect ratio of the source video.
helpviewer_keywords: ["IVMRAspectRatioControl","IVMRAspectRatioControl interface [DirectShow]","IVMRAspectRatioControl interface [DirectShow]","described","IVMRAspectRatioControlInterface","dshow.ivmraspectratiocontrol","strmif/IVMRAspectRatioControl"]
old-location: dshow\ivmraspectratiocontrol.htm
tech.root: dshow
ms.assetid: a341be9d-9801-4215-840d-7d581e9ec3cb
ms.date: 12/05/2018
ms.keywords: IVMRAspectRatioControl, IVMRAspectRatioControl interface [DirectShow], IVMRAspectRatioControl interface [DirectShow],described, IVMRAspectRatioControlInterface, dshow.ivmraspectratiocontrol, strmif/IVMRAspectRatioControl
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IVMRAspectRatioControl
 - strmif/IVMRAspectRatioControl
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
 - IVMRAspectRatioControl
---

# IVMRAspectRatioControl interface


## -description

The <code>IVMRAspectRatioControl</code> interface controls whether the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/video-mixing-renderer-filter-7">Video Mixing Renderer Filter 7</a> (VMR-7) preserves the aspect ratio of the source video. This interface is available when the VMR-7 is operating in either windowed or windowless modes. In windowless mode, the same functionality is provided by the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ivmrwindowlesscontrol">IVMRWindowlessControl</a> interface.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRAspectRatioControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRAspectRatioControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRAspectRatioControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmraspectratiocontrol-getaspectratiomode">GetAspectRatioMode</a>
</td>
<td align="left" width="63%">
Queries whether the VMR will preserve the aspect ratio of the source video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmraspectratiocontrol-setaspectratiomode">SetAspectRatioMode</a>
</td>
<td align="left" width="63%">
Specifies whether the VMR will preserve the aspect ratio of the source video.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>

