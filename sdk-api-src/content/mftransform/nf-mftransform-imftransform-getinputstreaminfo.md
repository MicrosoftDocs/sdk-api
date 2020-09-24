---
UID: NF:mftransform.IMFTransform.GetInputStreamInfo
title: IMFTransform::GetInputStreamInfo (mftransform.h)
description: Gets the buffer requirements and other information for an input stream on this Media Foundation transform (MFT).
helpviewer_keywords: ["GetInputStreamInfo","GetInputStreamInfo method [Media Foundation]","GetInputStreamInfo method [Media Foundation]","IMFTransform interface","IMFTransform interface [Media Foundation]","GetInputStreamInfo method","IMFTransform.GetInputStreamInfo","IMFTransform::GetInputStreamInfo","d57ffac7-1a92-4c6b-bd59-0acd7239c0a6","mf.imftransform_getinputstreaminfo","mftransform/IMFTransform::GetInputStreamInfo"]
old-location: mf\imftransform_getinputstreaminfo.htm
tech.root: mf
ms.assetid: d57ffac7-1a92-4c6b-bd59-0acd7239c0a6
ms.date: 12/05/2018
ms.keywords: GetInputStreamInfo, GetInputStreamInfo method [Media Foundation], GetInputStreamInfo method [Media Foundation],IMFTransform interface, IMFTransform interface [Media Foundation],GetInputStreamInfo method, IMFTransform.GetInputStreamInfo, IMFTransform::GetInputStreamInfo, d57ffac7-1a92-4c6b-bd59-0acd7239c0a6, mf.imftransform_getinputstreaminfo, mftransform/IMFTransform::GetInputStreamInfo
req.header: mftransform.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IMFTransform::GetInputStreamInfo
 - mftransform/IMFTransform::GetInputStreamInfo
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
 - IMFTransform.GetInputStreamInfo
---

# IMFTransform::GetInputStreamInfo


## -description

Gets the buffer requirements and other information for an input stream on this Media Foundation transform (MFT).

## -parameters

### -param dwInputStreamID [in]

Input stream identifier. To get the list of stream identifiers, call <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids">IMFTransform::GetStreamIDs</a>.

### -param pStreamInfo [out]

Pointer to an <a href="/windows/desktop/api/mftransform/ns-mftransform-mft_input_stream_info">MFT_INPUT_STREAM_INFO</a> structure. The method fills the structure with information about the input stream.

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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream identifier.
              

</td>
</tr>
</table>

## -remarks

It is valid to call this method before setting the media types. Note that the results of this call can change dynamically after the media type changes and after <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput">ProcessInput</a> is called, so you may need to call this method again after either of these occur.

If <b>MFT_UNIQUE_METHOD_NAMES</b> is defined before including mftransform.h, this method is renamed <b>MFTGetInputStreamInfo</b>. See <a href="/windows/desktop/medfound/comparison-of-mfts-and-dmos">Creating Hybrid DMO/MFT Objects</a>.

## -see-also

<a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a>



<a href="/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>