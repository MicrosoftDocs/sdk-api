---
UID: NS:opmapi._OPM_GET_CODEC_INFO_INFORMATION
title: OPM_GET_CODEC_INFO_INFORMATION (opmapi.h)

description: Contains the result from an OPM_GET_CODEC_INFO query.
old-location: mf\opm_get_codec_info_information.htm
tech.root: medfound
ms.assetid: 20865210-7f0f-4310-879e-9d1fe97f5df2

ms.date: 12/05/2018
ms.keywords: OPM_GET_CODEC_INFO_INFORMATION, OPM_GET_CODEC_INFO_INFORMATION structure [Media Foundation], _OPM_GET_CODEC_INFO_INFORMATION, ksopmapi/OPM_GET_CODEC_INFO_INFORMATION, mf.opm_get_codec_info_information
ms.topic: struct
f1_keywords:
- opmapi/OPM_GET_CODEC_INFO_INFORMATION
dev_langs:
 - c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- ksopmapi.h
api_name:
- OPM_GET_CODEC_INFO_INFORMATION
targetos: Windows
req.typenames: OPM_GET_CODEC_INFO_INFORMATION
req.redist: 
ms.custom: 19H1
---

# OPM_GET_CODEC_INFO_INFORMATION structure


## -description


Contains the result from an <a href="https://docs.microsoft.com/windows/desktop/medfound/opm-get-codec-info">OPM_GET_CODEC_INFO</a> query.


## -struct-fields




### -field rnRandomNumber

An <a href="https://docs.microsoft.com/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_random_number">OPM_RANDOM_NUMBER</a> structure. This structure contains the same 128-bit random number that the application sent to the driver in the <a href="https://docs.microsoft.com/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters">OPM_GET_INFO_PARAMETERS</a> structure.


### -field Merit

The merit value of the codec.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/opm-structures">OPM Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a>
 

 

