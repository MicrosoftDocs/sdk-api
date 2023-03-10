---
UID: NS:opmapi._OPM_GET_CODEC_INFO_INFORMATION
title: OPM_GET_CODEC_INFO_INFORMATION (opmapi.h)
description: OPM_GET_CODEC_INFO_INFORMATION (opmapi.h) contains the result from an OPM_GET_CODEC_INFO query.
helpviewer_keywords: ["OPM_GET_CODEC_INFO_INFORMATION","OPM_GET_CODEC_INFO_INFORMATION structure [Media Foundation]","_OPM_GET_CODEC_INFO_INFORMATION","ksopmapi/OPM_GET_CODEC_INFO_INFORMATION","mf.opm_get_codec_info_information"]
old-location: mf\opm_get_codec_info_information.htm
tech.root: mf
ms.assetid: 20865210-7f0f-4310-879e-9d1fe97f5df2
ms.date: 08/02/2022
ms.keywords: OPM_GET_CODEC_INFO_INFORMATION, OPM_GET_CODEC_INFO_INFORMATION structure [Media Foundation], _OPM_GET_CODEC_INFO_INFORMATION, ksopmapi/OPM_GET_CODEC_INFO_INFORMATION, mf.opm_get_codec_info_information
req.header: opmapi.h
req.include-header: Opmapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: OPM_GET_CODEC_INFO_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OPM_GET_CODEC_INFO_INFORMATION
 - opmapi/_OPM_GET_CODEC_INFO_INFORMATION
 - OPM_GET_CODEC_INFO_INFORMATION
 - opmapi/OPM_GET_CODEC_INFO_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ksopmapi.h
api_name:
 - OPM_GET_CODEC_INFO_INFORMATION
---

# OPM_GET_CODEC_INFO_INFORMATION structure


## -description

Contains the result from an <a href="/windows/desktop/medfound/opm-get-codec-info">OPM_GET_CODEC_INFO</a> query.

## -struct-fields

### -field rnRandomNumber

An <a href="/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_random_number">OPM_RANDOM_NUMBER</a> structure. This structure contains the same 128-bit random number that the application sent to the driver in the <a href="/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters">OPM_GET_INFO_PARAMETERS</a> structure.

### -field Merit

The merit value of the codec.

## -see-also

<a href="/windows/desktop/medfound/opm-structures">OPM Structures</a>



<a href="/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a>
