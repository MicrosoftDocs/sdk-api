---
UID: NE:mftransform._MFT_PROCESS_OUTPUT_STATUS
title: _MFT_PROCESS_OUTPUT_STATUS (mftransform.h)
description: Indicates the status of a call to IMFTransform::ProcessOutput.
helpviewer_keywords: ["80804b33-1dac-41f8-8446-8f929bf9b931","MFT_PROCESS_OUTPUT_STATUS_NEW_STREAMS","_MFT_PROCESS_OUTPUT_STATUS","_MFT_PROCESS_OUTPUT_STATUS enumeration [Media Foundation]","mf._mft_process_output_status","mftransform/MFT_PROCESS_OUTPUT_STATUS_NEW_STREAMS","mftransform/_MFT_PROCESS_OUTPUT_STATUS"]
old-location: mf\_mft_process_output_status.htm
tech.root: mf
ms.assetid: 80804b33-1dac-41f8-8446-8f929bf9b931
ms.date: 12/05/2018
ms.keywords: 80804b33-1dac-41f8-8446-8f929bf9b931, MFT_PROCESS_OUTPUT_STATUS_NEW_STREAMS, _MFT_PROCESS_OUTPUT_STATUS, _MFT_PROCESS_OUTPUT_STATUS enumeration [Media Foundation], mf._mft_process_output_status, mftransform/MFT_PROCESS_OUTPUT_STATUS_NEW_STREAMS, mftransform/_MFT_PROCESS_OUTPUT_STATUS
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFT_PROCESS_OUTPUT_STATUS
 - mftransform/_MFT_PROCESS_OUTPUT_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mftransform.h
api_name:
 - _MFT_PROCESS_OUTPUT_STATUS
---

# _MFT_PROCESS_OUTPUT_STATUS enumeration


## -description

Indicates the status of a call to <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">IMFTransform::ProcessOutput</a>.

## -enum-fields

### -field MFT_PROCESS_OUTPUT_STATUS_NEW_STREAMS:0x100

The Media Foundation transform (MFT) has created one or more new output streams.

## -remarks

If the MFT sets this flag, the <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">ProcessOutput</a> method returns MF_E_TRANSFORM_STREAM_CHANGE and no output data is produced. The client should respond as follows:

<ol>
<li>
Call <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount">IMFTransform::GetStreamCount</a> to get the new number of streams.

</li>
<li>
Call <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids">IMFTransform::GetStreamIDs</a> to get the new stream identifiers.

</li>
<li>
Call <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype">IMFTransform::GetOutputAvailableType</a> and <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype">IMFTransform::SetOutputType</a> to set the media types on the new streams.

</li>
</ol>
Until these steps are completed, all further calls to <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">ProcessOutput</a> return MF_E_TRANSFORM_STREAM_CHANGE.

## -see-also

<a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">IMFTransform::ProcessOutput</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>



<a href="/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>
