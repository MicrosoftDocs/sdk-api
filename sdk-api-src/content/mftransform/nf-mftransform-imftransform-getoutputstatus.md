---
UID: NF:mftransform.IMFTransform.GetOutputStatus
title: IMFTransform::GetOutputStatus (mftransform.h)
description: Queries whether the Media Foundation transform (MFT) is ready to produce output data.
helpviewer_keywords: ["3eb82f76-088b-4abc-9f3a-dfa5ecd1068d","GetOutputStatus","GetOutputStatus method [Media Foundation]","GetOutputStatus method [Media Foundation]","IMFTransform interface","IMFTransform interface [Media Foundation]","GetOutputStatus method","IMFTransform.GetOutputStatus","IMFTransform::GetOutputStatus","mf.imftransform_getoutputstatus","mftransform/IMFTransform::GetOutputStatus"]
old-location: mf\imftransform_getoutputstatus.htm
tech.root: mf
ms.assetid: 3eb82f76-088b-4abc-9f3a-dfa5ecd1068d
ms.date: 12/05/2018
ms.keywords: 3eb82f76-088b-4abc-9f3a-dfa5ecd1068d, GetOutputStatus, GetOutputStatus method [Media Foundation], GetOutputStatus method [Media Foundation],IMFTransform interface, IMFTransform interface [Media Foundation],GetOutputStatus method, IMFTransform.GetOutputStatus, IMFTransform::GetOutputStatus, mf.imftransform_getoutputstatus, mftransform/IMFTransform::GetOutputStatus
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
 - IMFTransform::GetOutputStatus
 - mftransform/IMFTransform::GetOutputStatus
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
 - IMFTransform.GetOutputStatus
---

# IMFTransform::GetOutputStatus


## -description

Queries whether the Media Foundation transform (MFT) is ready to produce output data.

## -parameters

### -param pdwFlags [out]

Receives a member of the <a href="/windows/win32/api/mftransform/ne-mftransform-_mft_output_status_flags">_MFT_OUTPUT_STATUS_FLAGS</a> enumeration, or zero. If the value is <b>MFT_OUTPUT_STATUS_SAMPLE_READY</b>, the MFT can produce an output sample.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.
              

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

If the method returns the <b>MFT_OUTPUT_STATUS_SAMPLE_READY</b> flag, it means you can generate one or more output samples by calling <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">IMFTransform::ProcessOutput</a>.
      

MFTs are not required to implement this method. If the method returns <b>E_NOTIMPL</b>, you must call <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">ProcessOutput</a> to determine whether the transform has output data.
      

If the MFT has more than one output stream, but it does not produce samples at the same time for each stream, it can set the <b>MFT_OUTPUT_STATUS_SAMPLE_READY</b> flag when just one stream is ready. However, if the MFT normally produces samples at the same time for each output stream, it should not set this flag until all streams are ready.
      

After the client has set valid media types on all of the streams, the MFT should always be in one of two states: Able to accept more input, or able to produce more output.
      

If <b>MFT_UNIQUE_METHOD_NAMES</b> is defined before including mftransform.h, this method is renamed <b>MFTGetOutputStatus</b>. See <a href="/windows/desktop/medfound/comparison-of-mfts-and-dmos">Creating Hybrid DMO/MFT Objects</a>.

## -see-also

<a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a>



<a href="/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>