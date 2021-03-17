---
UID: NF:amvideo.IDirectDrawVideo.GetSwitches
title: IDirectDrawVideo::GetSwitches (amvideo.h)
description: The GetSwitches method retrieves the surface types that the renderer is allowed to use.
helpviewer_keywords: ["GetSwitches","GetSwitches method [DirectShow]","GetSwitches method [DirectShow]","IDirectDrawVideo interface","IDirectDrawVideo interface [DirectShow]","GetSwitches method","IDirectDrawVideo.GetSwitches","IDirectDrawVideo::GetSwitches","IDirectDrawVideoGetSwitches","amvideo/IDirectDrawVideo::GetSwitches","dshow.idirectdrawvideo_getswitches"]
old-location: dshow\idirectdrawvideo_getswitches.htm
tech.root: dshow
ms.assetid: 0a9e3c46-6d2d-474e-ab72-f67b5ed450f2
ms.date: 12/05/2018
ms.keywords: GetSwitches, GetSwitches method [DirectShow], GetSwitches method [DirectShow],IDirectDrawVideo interface, IDirectDrawVideo interface [DirectShow],GetSwitches method, IDirectDrawVideo.GetSwitches, IDirectDrawVideo::GetSwitches, IDirectDrawVideoGetSwitches, amvideo/IDirectDrawVideo::GetSwitches, dshow.idirectdrawvideo_getswitches
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectDrawVideo::GetSwitches
 - amvideo/IDirectDrawVideo::GetSwitches
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
 - IDirectDrawVideo.GetSwitches
---

# IDirectDrawVideo::GetSwitches


## -description

The <code>GetSwitches</code> method retrieves the surface types that the renderer is allowed to use.

## -parameters

### -param pSwitches

Pointer to a bit mask containing one or more of the following DirectShow DirectDraw Surface (AMDDS) surface types.

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

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-idirectdrawvideo">IDirectDrawVideo Interface</a>