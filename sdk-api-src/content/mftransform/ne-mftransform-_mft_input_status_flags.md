---
UID: NE:mftransform._MFT_INPUT_STATUS_FLAGS
title: _MFT_INPUT_STATUS_FLAGS (mftransform.h)
description: Indicates the status of an input stream on a Media Foundation transform (MFT).
helpviewer_keywords: ["MFT_INPUT_STATUS_ACCEPT_DATA","_MFT_INPUT_STATUS_FLAGS","_MFT_INPUT_STATUS_FLAGS enumeration [Media Foundation]","c63052a1-58b6-4537-9214-6f8d79a9eafd","mf._mft_input_status_flags","mftransform/MFT_INPUT_STATUS_ACCEPT_DATA","mftransform/_MFT_INPUT_STATUS_FLAGS"]
old-location: mf\_mft_input_status_flags.htm
tech.root: mf
ms.assetid: c63052a1-58b6-4537-9214-6f8d79a9eafd
ms.date: 12/05/2018
ms.keywords: MFT_INPUT_STATUS_ACCEPT_DATA, _MFT_INPUT_STATUS_FLAGS, _MFT_INPUT_STATUS_FLAGS enumeration [Media Foundation], c63052a1-58b6-4537-9214-6f8d79a9eafd, mf._mft_input_status_flags, mftransform/MFT_INPUT_STATUS_ACCEPT_DATA, mftransform/_MFT_INPUT_STATUS_FLAGS
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
 - _MFT_INPUT_STATUS_FLAGS
 - mftransform/_MFT_INPUT_STATUS_FLAGS
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
 - _MFT_INPUT_STATUS_FLAGS
---

# _MFT_INPUT_STATUS_FLAGS enumeration


## -description

Indicates the status of an input stream on a Media Foundation transform (MFT).

## -enum-fields

### -field MFT_INPUT_STATUS_ACCEPT_DATA:0x1

The input stream can receive more data at this time. To deliver more input data, call <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput">IMFTransform::ProcessInput</a>.

## -see-also

<a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstatus">IMFTransform::GetInputStatus</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>



<a href="/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>
