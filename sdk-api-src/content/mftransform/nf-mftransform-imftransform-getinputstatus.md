---
UID: NF:mftransform.IMFTransform.GetInputStatus
title: IMFTransform::GetInputStatus (mftransform.h)
description: Queries whether an input stream on this Media Foundation transform (MFT) can accept more data.
helpviewer_keywords: ["6205dc1a-f209-49aa-8632-837783ef5f04","GetInputStatus","GetInputStatus method [Media Foundation]","GetInputStatus method [Media Foundation]","IMFTransform interface","IMFTransform interface [Media Foundation]","GetInputStatus method","IMFTransform.GetInputStatus","IMFTransform::GetInputStatus","mf.imftransform_getinputstatus","mftransform/IMFTransform::GetInputStatus"]
old-location: mf\imftransform_getinputstatus.htm
tech.root: mf
ms.assetid: 6205dc1a-f209-49aa-8632-837783ef5f04
ms.date: 12/05/2018
ms.keywords: 6205dc1a-f209-49aa-8632-837783ef5f04, GetInputStatus, GetInputStatus method [Media Foundation], GetInputStatus method [Media Foundation],IMFTransform interface, IMFTransform interface [Media Foundation],GetInputStatus method, IMFTransform.GetInputStatus, IMFTransform::GetInputStatus, mf.imftransform_getinputstatus, mftransform/IMFTransform::GetInputStatus
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
 - IMFTransform::GetInputStatus
 - mftransform/IMFTransform::GetInputStatus
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
 - IMFTransform.GetInputStatus
---

# IMFTransform::GetInputStatus


## -description

Queries whether an input stream on this Media Foundation transform (MFT) can accept more data.

## -parameters

### -param dwInputStreamID [in]

Input stream identifier. To get the list of stream identifiers, call <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids">IMFTransform::GetStreamIDs</a>.

### -param pdwFlags [out]

Receives a member of the <a href="/windows/win32/api/mftransform/ne-mftransform-_mft_input_status_flags">_MFT_INPUT_STATUS_FLAGS</a> enumeration, or zero. If the value is <b>MFT_INPUT_STATUS_ACCEPT_DATA</b>, the stream specified in <i>dwInputStreamID</i> can accept more input data.

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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_TRANSFORM_TYPE_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
The media type is not set on one or more streams.
              

</td>
</tr>
</table>

## -remarks

If the method returns the <b>MFT_INPUT_STATUS_ACCEPT_DATA</b> flag, you can deliver an input sample to the specified stream by calling <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput">IMFTransform::ProcessInput</a>. If the method succeeds but does not return any flags in the <i>pdwFlags</i> parameter, it means the input stream already has as much data as it can accept.
      

Use this method to test whether the input stream is ready to accept more data, without incurring the overhead of allocating a new sample and calling <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput">ProcessInput</a>.
      

After the client has set valid media types on all of the streams, the MFT should always be in one of two states: Able to accept more input, or able to produce more output (or both).
      

If <b>MFT_UNIQUE_METHOD_NAMES</b> is defined before including mftransform.h, this method is renamed <b>MFTGetInputStatus</b>. See <a href="/windows/desktop/medfound/comparison-of-mfts-and-dmos">Creating Hybrid DMO/MFT Objects</a>.

## -see-also

<a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a>



<a href="/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>