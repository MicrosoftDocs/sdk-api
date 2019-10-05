---
UID: NN:strmif.IVMRSurface
title: IVMRSurface (strmif.h)
author: windows-sdk-content
description: The IVMRSurface interface is implemented on the media samples used by the Video Mixing Renderer Filter 7 (VMR-7).
old-location: dshow\ivmrsurface.htm
tech.root: DirectShow
ms.assetid: 8222ea5c-be77-4f33-83ff-073fb3e85e73
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVMRSurface, IVMRSurface interface [DirectShow], IVMRSurface interface [DirectShow],described, IVMRSurfaceInterface, dshow.ivmrsurface, strmif/IVMRSurface
ms.topic: interface
f1_keywords: 
 - "strmif/IVMRSurface"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRSurface
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRSurface interface


## -description



The <code>IVMRSurface</code> interface is implemented on the media samples used by the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/video-mixing-renderer-filter-7">Video Mixing Renderer Filter 7</a> (VMR-7). Filters can use this interface to access the underlying DirectDraw surface on which the media sample is based. Filters must always lock and unlock the surface using the methods available on this interface. Filters must never call lock or unlock directly on the DirectDraw surface interface returned from the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrsurface-getsurface">GetSurface</a> method. Applications do not use this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRSurface</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRSurface</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRSurface</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrsurface-getsurface">GetSurface</a>
</td>
<td align="left" width="63%">
Retrieves the attached DirectDraw surface interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrsurface-issurfacelocked">IsSurfaceLocked</a>
</td>
<td align="left" width="63%">
Indicates whether the DirectDraw surface attached to this media sample is locked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrsurface-locksurface">LockSurface</a>
</td>
<td align="left" width="63%">
Locks the attached DirectDraw surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrsurface-unlocksurface">UnlockSurface</a>
</td>
<td align="left" width="63%">
Unlocks the attached DirectDraw surface.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

