---
UID: NN:strmif.IVMRSurface
title: IVMRSurface
author: windows-sdk-content
description: The IVMRSurface interface is implemented on the media samples used by the Video Mixing Renderer Filter 7 (VMR-7).
old-location: dshow\ivmrsurface.htm
old-project: DirectShow
ms.assetid: 8222ea5c-be77-4f33-83ff-073fb3e85e73
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IVMRSurface, IVMRSurface interface [DirectShow], IVMRSurface interface [DirectShow],described, IVMRSurfaceInterface, dshow.ivmrsurface, strmif/IVMRSurface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.redist: 
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
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
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRSurface interface


## -description



The <code>IVMRSurface</code> interface is implemented on the media samples used by the <a href="https://msdn.microsoft.com/c83e6c50-76f2-4aeb-944b-5b244c6bf776">Video Mixing Renderer Filter 7</a> (VMR-7). Filters can use this interface to access the underlying DirectDraw surface on which the media sample is based. Filters must always lock and unlock the surface using the methods available on this interface. Filters must never call lock or unlock directly on the DirectDraw surface interface returned from the <a href="https://msdn.microsoft.com/2fba7818-6395-47d3-98b3-347f1d4a7c6f">GetSurface</a> method. Applications do not use this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRSurface</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVMRSurface</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/2fba7818-6395-47d3-98b3-347f1d4a7c6f">GetSurface</a>
</td>
<td align="left" width="63%">
Retrieves the attached DirectDraw surface interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/690194c2-2f40-414f-9130-f2f9c44fe71e">IsSurfaceLocked</a>
</td>
<td align="left" width="63%">
Indicates whether the DirectDraw surface attached to this media sample is locked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/119a6983-3639-4047-b8b4-7a8b0cb5583d">LockSurface</a>
</td>
<td align="left" width="63%">
Locks the attached DirectDraw surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f6acaf96-925c-46b9-8d56-11d94f3dbda3">UnlockSurface</a>
</td>
<td align="left" width="63%">
Unlocks the attached DirectDraw surface.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

