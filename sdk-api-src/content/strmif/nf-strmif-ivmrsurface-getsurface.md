---
UID: NF:strmif.IVMRSurface.GetSurface
title: IVMRSurface::GetSurface (strmif.h)
author: windows-sdk-content
description: The GetSurface method retrieves the attached DirectDraw surface interface.
old-location: dshow\ivmrsurface_getsurface.htm
tech.root: DirectShow
ms.assetid: 2fba7818-6395-47d3-98b3-347f1d4a7c6f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSurface, GetSurface method [DirectShow], GetSurface method [DirectShow],IVMRSurface interface, IVMRSurface interface [DirectShow],GetSurface method, IVMRSurface.GetSurface, IVMRSurface::GetSurface, IVMRSurfaceGetSurface, dshow.ivmrsurface_getsurface, strmif/IVMRSurface::GetSurface
ms.topic: method
f1_keywords: 
 - "strmif/IVMRSurface.GetSurface"
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
 - IVMRSurface.GetSurface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRSurface::GetSurface


## -description



The <code>GetSurface</code> method retrieves the attached DirectDraw surface interface.




## -parameters




### -param lplpSurface [out]

Address of a variable that receives a pointer to the <b>IDirectDrawSurface7</b> interface. The caller must release the interface.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
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
 

 

