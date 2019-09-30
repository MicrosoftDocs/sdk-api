---
UID: NF:strmif.IVMRSurface.UnlockSurface
title: IVMRSurface::UnlockSurface (strmif.h)
author: windows-sdk-content
description: The UnlockSurface method unlocks the attached DirectDraw surface.
old-location: dshow\ivmrsurface_unlocksurface.htm
tech.root: DirectShow
ms.assetid: f6acaf96-925c-46b9-8d56-11d94f3dbda3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVMRSurface interface [DirectShow],UnlockSurface method, IVMRSurface.UnlockSurface, IVMRSurface::UnlockSurface, IVMRSurfaceUnlockSurface, UnlockSurface, UnlockSurface method [DirectShow], UnlockSurface method [DirectShow],IVMRSurface interface, dshow.ivmrsurface_unlocksurface, strmif/IVMRSurface::UnlockSurface
ms.topic: method
f1_keywords: 
 - "strmif/IVMRSurface.UnlockSurface"
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
 - IVMRSurface.UnlockSurface
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRSurface::UnlockSurface


## -description



The <code>UnlockSurface</code> method unlocks the attached DirectDraw surface.




## -parameters






## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
No DirectDraw surface is attached to this sample.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ivmrsurface">IVMRSurface Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

