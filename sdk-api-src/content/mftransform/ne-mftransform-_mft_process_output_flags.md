---
UID: NE:mftransform._MFT_PROCESS_OUTPUT_FLAGS
title: _MFT_PROCESS_OUTPUT_FLAGS (mftransform.h)
description: Defines flags for processing output samples in a Media Foundation transform (MFT).
helpviewer_keywords: ["846e91a5-7cd8-4b58-9484-b9cb9af0bebf","MFT_PROCESS_OUTPUT_DISCARD_WHEN_NO_BUFFER","MFT_PROCESS_OUTPUT_REGENERATE_LAST_OUTPUT","_MFT_PROCESS_OUTPUT_FLAGS","_MFT_PROCESS_OUTPUT_FLAGS enumeration [Media Foundation]","mf._mft_process_output_flags","mftransform/MFT_PROCESS_OUTPUT_DISCARD_WHEN_NO_BUFFER","mftransform/MFT_PROCESS_OUTPUT_REGENERATE_LAST_OUTPUT","mftransform/_MFT_PROCESS_OUTPUT_FLAGS"]
old-location: mf\_mft_process_output_flags.htm
tech.root: mf
ms.assetid: 846e91a5-7cd8-4b58-9484-b9cb9af0bebf
ms.date: 12/05/2018
ms.keywords: 846e91a5-7cd8-4b58-9484-b9cb9af0bebf, MFT_PROCESS_OUTPUT_DISCARD_WHEN_NO_BUFFER, MFT_PROCESS_OUTPUT_REGENERATE_LAST_OUTPUT, _MFT_PROCESS_OUTPUT_FLAGS, _MFT_PROCESS_OUTPUT_FLAGS enumeration [Media Foundation], mf._mft_process_output_flags, mftransform/MFT_PROCESS_OUTPUT_DISCARD_WHEN_NO_BUFFER, mftransform/MFT_PROCESS_OUTPUT_REGENERATE_LAST_OUTPUT, mftransform/_MFT_PROCESS_OUTPUT_FLAGS
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
 - _MFT_PROCESS_OUTPUT_FLAGS
 - mftransform/_MFT_PROCESS_OUTPUT_FLAGS
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
 - _MFT_PROCESS_OUTPUT_FLAGS
---

# _MFT_PROCESS_OUTPUT_FLAGS enumeration


## -description

Defines flags for processing output samples in a Media Foundation transform (MFT).

## -enum-fields

### -field MFT_PROCESS_OUTPUT_DISCARD_WHEN_NO_BUFFER:0x1

Do not produce output for streams in which the <b>pSample</b> member of the <a href="/windows/desktop/api/mftransform/ns-mftransform-mft_output_data_buffer">MFT_OUTPUT_DATA_BUFFER</a> structure is <b>NULL</b>. This flag is not valid unless the MFT has marked the output stream with the MFT_OUTPUT_STREAM_DISCARDABLE or MFT_OUTPUT_STREAM_LAZY_READ flag. For more information, see <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo">IMFTransform::GetOutputStreamInfo</a>.

### -field MFT_PROCESS_OUTPUT_REGENERATE_LAST_OUTPUT:0x2

Regenerates the last output sample. This flag is only used by video processing MFTs.

<b>Note</b> Requires Windows 8.

## -see-also

<a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">IMFTransform::ProcessOutput</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>



<a href="/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>
