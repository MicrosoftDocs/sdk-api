---
UID: NF:amvideo.IDirectDrawVideo.GetSurfaceType
title: IDirectDrawVideo::GetSurfaceType
author: windows-sdk-content
description: The GetSurfaceType method retrieves the actual surface type as a DirectShow DirectDraw Surface (AMDDS) definition.
old-location: dshow\idirectdrawvideo_getsurfacetype.htm
tech.root: DirectShow
ms.assetid: f5d5c608-1890-43f8-bdf3-3fcb0c6a2f5e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetSurfaceType, GetSurfaceType method [DirectShow], GetSurfaceType method [DirectShow],IDirectDrawVideo interface, IDirectDrawVideo interface [DirectShow],GetSurfaceType method, IDirectDrawVideo.GetSurfaceType, IDirectDrawVideo::GetSurfaceType, IDirectDrawVideoGetSurfaceType, amvideo/IDirectDrawVideo::GetSurfaceType, dshow.idirectdrawvideo_getsurfacetype
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd406816(v=VS.85).aspx">IDirectDrawVideo Interface</a>
 

 

