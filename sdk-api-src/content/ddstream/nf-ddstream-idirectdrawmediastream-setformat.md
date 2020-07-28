---
UID: NF:ddstream.IDirectDrawMediaStream.SetFormat
title: IDirectDrawMediaStream::SetFormat (ddstream.h)
description: Note  This interface is deprecated. New applications should not use it. Sets the format of the current media stream.
helpviewer_keywords: ["IDirectDrawMediaStream interface [DirectShow]","SetFormat method","IDirectDrawMediaStream.SetFormat","IDirectDrawMediaStream::SetFormat","IDirectDrawMediaStreamSetFormat","SetFormat","SetFormat method [DirectShow]","SetFormat method [DirectShow]","IDirectDrawMediaStream interface","ddstream/IDirectDrawMediaStream::SetFormat","dshow.idirectdrawmediastream_setformat"]
old-location: dshow\idirectdrawmediastream_setformat.htm
tech.root: dshow
ms.assetid: 465b4f0c-40e1-4aec-be62-0b55c29fa05e
ms.date: 12/05/2018
ms.keywords: IDirectDrawMediaStream interface [DirectShow],SetFormat method, IDirectDrawMediaStream.SetFormat, IDirectDrawMediaStream::SetFormat, IDirectDrawMediaStreamSetFormat, SetFormat, SetFormat method [DirectShow], SetFormat method [DirectShow],IDirectDrawMediaStream interface, ddstream/IDirectDrawMediaStream::SetFormat, dshow.idirectdrawmediastream_setformat
f1_keywords:
- ddstream/IDirectDrawMediaStream.SetFormat
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- ddstream.h
api_name:
- IDirectDrawMediaStream.SetFormat
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectDrawMediaStream::SetFormat


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Sets the format of the current media stream.




## -parameters




### -param pDDSurfaceDesc [in]

Pointer to a DirectDraw surface description that contains the new format.


### -param pDirectDrawPalette [in]

Optional parameter that is a pointer to an <b>IDirectDrawPalette</b> interface.


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
<dt><b>DDERR_INVALIDSURFACETYPE</b></dt>
</dl>
</td>
<td width="60%">
The specified format is incompatible with the current stream.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MS_E_SAMPLEALLOC</b></dt>
</dl>
</td>
<td width="60%">
Can't change the format because one or more stream samples are already allocated for this stream.

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



If the stream already has allocated samples and the sample format doesn't match the specified format, this method fails. This method always succeeds if the specified format matches the current format.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream">IDirectDrawMediaStream Interface</a>
 

 

