---
UID: NF:amvideo.IDirectDrawVideo.SetSwitches
title: IDirectDrawVideo::SetSwitches
author: windows-sdk-content
description: The SetSwitches method sets the surface types that the renderer is allowed to use.
old-location: dshow\idirectdrawvideo_setswitches.htm
old-project: DirectShow
ms.assetid: e6839757-2b63-497d-9978-35c8dfabc0ed
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IDirectDrawVideo interface [DirectShow],SetSwitches method, IDirectDrawVideo.SetSwitches, IDirectDrawVideo::SetSwitches, IDirectDrawVideoSetSwitches, SetSwitches, SetSwitches method [DirectShow], SetSwitches method [DirectShow],IDirectDrawVideo interface, amvideo/IDirectDrawVideo::SetSwitches, dshow.idirectdrawvideo_setswitches
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: amvideo.h
req.include-header: Dshow.h
req.redist: 
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
tech.root: 
req.typenames: AMVAUncompDataInfo, *LPAMVAUncompDataInfo
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDirectDrawVideo.SetSwitches
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IDirectDrawVideo::SetSwitches


## -description



The <code>SetSwitches</code> method sets the surface types that the renderer is allowed to use.




## -parameters




### -param Switches

Bit mask containing one or more of the following DirectShow DirectDraw Surface (AMDDS) surface types.

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



This method must be called before the Video Renderer is connected.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/b918bf3b-b91b-40fb-abb8-4115a4f254bb">IDirectDrawVideo Interface</a>
 

 

