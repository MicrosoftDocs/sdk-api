---
UID: NF:ddstream.IDirectDrawMediaStream.GetFormat
title: IDirectDrawMediaStream::GetFormat (ddstream.h)
description: Note  This interface is deprecated. New applications should not use it. Retrieves the current media stream's format and, optionally, its desired format.
helpviewer_keywords: ["GetFormat","GetFormat method [DirectShow]","GetFormat method [DirectShow]","IDirectDrawMediaStream interface","IDirectDrawMediaStream interface [DirectShow]","GetFormat method","IDirectDrawMediaStream.GetFormat","IDirectDrawMediaStream::GetFormat","IDirectDrawMediaStreamGetFormat","ddstream/IDirectDrawMediaStream::GetFormat","dshow.idirectdrawmediastream_getformat"]
old-location: dshow\idirectdrawmediastream_getformat.htm
tech.root: dshow
ms.assetid: 3729bbe6-3504-46b3-9978-e66afc56344f
ms.date: 12/05/2018
ms.keywords: GetFormat, GetFormat method [DirectShow], GetFormat method [DirectShow],IDirectDrawMediaStream interface, IDirectDrawMediaStream interface [DirectShow],GetFormat method, IDirectDrawMediaStream.GetFormat, IDirectDrawMediaStream::GetFormat, IDirectDrawMediaStreamGetFormat, ddstream/IDirectDrawMediaStream::GetFormat, dshow.idirectdrawmediastream_getformat
req.header: ddstream.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectDrawMediaStream::GetFormat
 - ddstream/IDirectDrawMediaStream::GetFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ddstream.h
api_name:
 - IDirectDrawMediaStream.GetFormat
---

# IDirectDrawMediaStream::GetFormat


## -description

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Retrieves the current media stream's format and, optionally, its desired format.

## -parameters

### -param pDDSDCurrent [out]

Pointer to a DirectDraw surface description that will contain the current media stream's format.

### -param ppDirectDrawPalette [out]

Address of a pointer to an <b>IDirectDrawPalette</b> interface if one exists.

### -param pDDSDDesired [out]

Pointer to a DirectDraw surface description that will contain the current media stream's desired format.

### -param pdwFlags [out]

Pointer to the flags set in a <b>DDSURFACEDESC</b> structure. Flags of interest include:

<table>
<tr>
<th>Flag
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>DDSD_CAPS</td>
<td>Indicates that the surface capability member of the structure is valid.</td>
</tr>
<tr>
<td>DDSD_HEIGHT</td>
<td>Indicates that the height member of the structure is valid.</td>
</tr>
<tr>
<td>DDSD_PIXELFORMAT</td>
<td>Indicates that the pixel format member of the structure is valid.</td>
</tr>
<tr>
<td>DDSD_WIDTH</td>
<td>Indicates that the width member of the structure is valid.</td>
</tr>
</table>

## -returns

Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DDERR_INVALIDPARAMS</b></dt>
</dl>
</td>
<td width="60%">
One of the DirectDraw surface parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the required parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -remarks

After you call this method, you can either conform to the current format or attempt to change the format by calling the <a href="/windows/desktop/api/ddstream/nf-ddstream-idirectdrawmediastream-setformat">IDirectDrawMediaStream::SetFormat</a> method.

All of this method's parameters are optional; set any of them to <b>NULL</b> to indicate that you don't want to retrieve that information.

To perform a progressive render, create a single sample and repeatedly use that sample for successive frames of video. Video decompressors use this technique to do partial updates to the previous frame.

You must initialize the <i>dwSize</i> member of the <b>DDSURFACEDESC</b> structure before calling this method.

The DDSD_CAPS flag will return one of the values listed in the <b>DDSCAPS</b> structure or DDSCAPS_DATAEXCHANGE, which is defined as DDSCAPS_SYSTEMMEMORY|DDSCAPS_VIDEOMEMORY in Ddrawex.h.

## -see-also

<a href="/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream">IDirectDrawMediaStream Interface</a>