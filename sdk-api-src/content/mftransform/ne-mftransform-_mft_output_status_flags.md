---
UID: NE:mftransform._MFT_OUTPUT_STATUS_FLAGS
title: _MFT_OUTPUT_STATUS_FLAGS (mftransform.h)
description: Indicates whether a Media Foundation transform (MFT) can produce output data.
helpviewer_keywords: ["951900b1-364e-4867-a1f8-50d485d13c77","MFT_OUTPUT_STATUS_SAMPLE_READY","_MFT_OUTPUT_STATUS_FLAGS","_MFT_OUTPUT_STATUS_FLAGS enumeration [Media Foundation]","mf._mft_output_status_flags","mftransform/MFT_OUTPUT_STATUS_SAMPLE_READY","mftransform/_MFT_OUTPUT_STATUS_FLAGS"]
old-location: mf\_mft_output_status_flags.htm
tech.root: mf
ms.assetid: 951900b1-364e-4867-a1f8-50d485d13c77
ms.date: 12/05/2018
ms.keywords: 951900b1-364e-4867-a1f8-50d485d13c77, MFT_OUTPUT_STATUS_SAMPLE_READY, _MFT_OUTPUT_STATUS_FLAGS, _MFT_OUTPUT_STATUS_FLAGS enumeration [Media Foundation], mf._mft_output_status_flags, mftransform/MFT_OUTPUT_STATUS_SAMPLE_READY, mftransform/_MFT_OUTPUT_STATUS_FLAGS
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
 - _MFT_OUTPUT_STATUS_FLAGS
 - mftransform/_MFT_OUTPUT_STATUS_FLAGS
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
 - _MFT_OUTPUT_STATUS_FLAGS
---

# _MFT_OUTPUT_STATUS_FLAGS enumeration


## -description

Indicates whether a Media Foundation transform (MFT) can produce output data.

## -enum-fields

### -field MFT_OUTPUT_STATUS_SAMPLE_READY:0x1

There is a sample available for at least one output stream. To retrieve the available output samples, call <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">IMFTransform::ProcessOutput</a>.

## -see-also

<a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstatus">IMFTransform::GetOutputStatus</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>



<a href="/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>
