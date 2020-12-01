---
UID: NF:mfobjects.IMFVideoMediaType.GetVideoRepresentation
title: IMFVideoMediaType::GetVideoRepresentation (mfobjects.h)
description: Retrieves an alternative representation of the media type.
helpviewer_keywords: ["2f8fddef-b9b8-4473-a8d0-d6e44ad32648","GetVideoRepresentation","GetVideoRepresentation method [Media Foundation]","GetVideoRepresentation method [Media Foundation]","IMFVideoMediaType interface","IMFVideoMediaType interface [Media Foundation]","GetVideoRepresentation method","IMFVideoMediaType.GetVideoRepresentation","IMFVideoMediaType::GetVideoRepresentation","mf.imfvideomediatype_getvideorepresentation","mfobjects/IMFVideoMediaType::GetVideoRepresentation"]
old-location: mf\imfvideomediatype_getvideorepresentation.htm
tech.root: mf
ms.assetid: 2f8fddef-b9b8-4473-a8d0-d6e44ad32648
ms.date: 12/05/2018
ms.keywords: 2f8fddef-b9b8-4473-a8d0-d6e44ad32648, GetVideoRepresentation, GetVideoRepresentation method [Media Foundation], GetVideoRepresentation method [Media Foundation],IMFVideoMediaType interface, IMFVideoMediaType interface [Media Foundation],GetVideoRepresentation method, IMFVideoMediaType.GetVideoRepresentation, IMFVideoMediaType::GetVideoRepresentation, mf.imfvideomediatype_getvideorepresentation, mfobjects/IMFVideoMediaType::GetVideoRepresentation
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFVideoMediaType::GetVideoRepresentation
 - mfobjects/IMFVideoMediaType::GetVideoRepresentation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFVideoMediaType.GetVideoRepresentation
---

# IMFVideoMediaType::GetVideoRepresentation


## -description

<p class="CCE_Message">[This API is not supported and may be altered or unavailable in the future. Instead, applications should set the <a href="/windows/desktop/medfound/mf-mt-default-stride-attribute">MF_MT_DEFAULT_STRIDE</a> attribute on the media type to specify the surface stride and then call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation">IMFMediaType::GetRepresentation</a>.]

Retrieves an alternative representation of the media type.

## -parameters

### -param guidRepresentation [in]

GUID that specifies the representation to retrieve. For a list of values, see <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation">IMFMediaType::GetRepresentation</a>.

### -param ppvRepresentation [out]

Receives a pointer to a structure that contains the representation. The method allocates the memory for the structure. The caller must release the memory by calling <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-freerepresentation">IMFMediaType::FreeRepresentation</a>.

### -param lStride [in]

Stride of the video surface, in bytes. If the stride is unknown, set this value to 0. If the value is 0, the method computes the stride from the image width and assumes that there is no padding.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

This method is equivalent to <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation">IMFMediaType::GetRepresentation</a> but includes the <i>lStride</i> parameter.

Instead of calling this method, applications should set the <a href="/windows/desktop/medfound/mf-mt-default-stride-attribute">MF_MT_DEFAULT_STRIDE</a> attribute on the media type to specify the surface stride and then call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation">IMFMediaType::GetRepresentation</a>.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype">IMFVideoMediaType</a>



<a href="/windows/desktop/medfound/media-types">Media Types</a>