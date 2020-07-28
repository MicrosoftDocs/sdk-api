---
UID: NF:amvideo.IDirectDrawVideo.GetSurfaceType
title: IDirectDrawVideo::GetSurfaceType (amvideo.h)
description: The GetSurfaceType method retrieves the actual surface type as a DirectShow DirectDraw Surface (AMDDS) definition.
helpviewer_keywords: ["GetSurfaceType","GetSurfaceType method [DirectShow]","GetSurfaceType method [DirectShow]","IDirectDrawVideo interface","IDirectDrawVideo interface [DirectShow]","GetSurfaceType method","IDirectDrawVideo.GetSurfaceType","IDirectDrawVideo::GetSurfaceType","IDirectDrawVideoGetSurfaceType","amvideo/IDirectDrawVideo::GetSurfaceType","dshow.idirectdrawvideo_getsurfacetype"]
old-location: dshow\idirectdrawvideo_getsurfacetype.htm
tech.root: dshow
ms.assetid: f5d5c608-1890-43f8-bdf3-3fcb0c6a2f5e
ms.date: 12/05/2018
ms.keywords: GetSurfaceType, GetSurfaceType method [DirectShow], GetSurfaceType method [DirectShow],IDirectDrawVideo interface, IDirectDrawVideo interface [DirectShow],GetSurfaceType method, IDirectDrawVideo.GetSurfaceType, IDirectDrawVideo::GetSurfaceType, IDirectDrawVideoGetSurfaceType, amvideo/IDirectDrawVideo::GetSurfaceType, dshow.idirectdrawvideo_getsurfacetype
f1_keywords:
- amvideo/IDirectDrawVideo.GetSurfaceType
dev_langs:
- c++
req.header: amvideo.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
- IDirectDrawVideo.GetSurfaceType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectDrawVideo::GetSurfaceType


## -description



The <code>GetSurfaceType</code> method retrieves the actual surface type as a DirectShow DirectDraw Surface (AMDDS) definition.




## -parameters




### -param pSurfaceType

Pointer to variable that receives a bitwise-<b>OR</b> of one or more of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>AMDDS_NONE</td>
<td>No use for DCI/DirectDraw.</td>
</tr>
<tr>
<td>AMDDS_DCIPS</td>
<td>Use DCI primary surface.</td>
</tr>
<tr>
<td>AMDDS_PS</td>
<td>Use DirectDraw primary surface.</td>
</tr>
<tr>
<td>AMDDS_RGBOVR</td>
<td>RGB overlay surfaces.</td>
</tr>
<tr>
<td>AMDDS_YUVOVR</td>
<td>YUV overlay surfaces.</td>
</tr>
<tr>
<td>AMDDS_RGBOFF</td>
<td>RGB off-screen surfaces.</td>
</tr>
<tr>
<td>AMDDS_YUVOFF</td>
<td>YUV off-screen surfaces.</td>
</tr>
<tr>
<td>AMDDS_RGBFLP</td>
<td>RGB flipping surfaces.</td>
</tr>
<tr>
<td>AMDDS_YUVFLP</td>
<td>YUV flipping surfaces.</td>
</tr>
<tr>
<td>AMDDS_ALL</td>
<td>All the previous flags.</td>
</tr>
<tr>
<td>AMDDS_DEFAULT</td>
<td>Use all available surfaces.</td>
</tr>
<tr>
<td>AMDDS_YUV</td>
<td>(AMDDS_YUVOFF | AMDDS_YUVOVR | AMDDS_YUVFLP).</td>
</tr>
<tr>
<td>AMDDS_RGB</td>
<td>(AMDDS_RGBOFF | AMDDS_RGBOVR | AMDDS_RGBFLP).</td>
</tr>
<tr>
<td>AMDDS_PRIMARY</td>
<td>(AMDDS_DCIPS | AMDDS_PS).</td>
</tr>
</table>
 


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



It is not always easy to discover which kind of surface is being used by looking at a <b>DDSURFACEDESC</b> structure. Therefore, an application can call <code>GetSurfaceType</code> to retrieve the surface type. The field will be filled in with one bit setting selected from the preceding list of AMDDS definitions.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nn-amvideo-idirectdrawvideo">IDirectDrawVideo Interface</a>
 

 

