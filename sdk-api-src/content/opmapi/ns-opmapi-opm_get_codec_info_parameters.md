---
UID: NS:opmapi._OPM_GET_CODEC_INFO_PARAMETERS
title: OPM_GET_CODEC_INFO_PARAMETERS (opmapi.h)
description: Contains information for the OPM_GET_CODEC_INFO command.helpviewer_keywords: ["OPM_GET_CODEC_INFO_PARAMETERS","OPM_GET_CODEC_INFO_PARAMETERS structure [Media Foundation]","_OPM_GET_CODEC_INFO_PARAMETERS","ksopmapi/OPM_GET_CODEC_INFO_PARAMETERS","mf.opm_get_codec_info_parameters"]
old-location: mf\opm_get_codec_info_parameters.htm
tech.root: medfound
ms.assetid: 9fb130e5-fd87-4a11-9c9e-7a106a091b35
ms.date: 12/05/2018
ms.keywords: OPM_GET_CODEC_INFO_PARAMETERS, OPM_GET_CODEC_INFO_PARAMETERS structure [Media Foundation], _OPM_GET_CODEC_INFO_PARAMETERS, ksopmapi/OPM_GET_CODEC_INFO_PARAMETERS, mf.opm_get_codec_info_parameters
f1_keywords:
- opmapi/OPM_GET_CODEC_INFO_PARAMETERS
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
- OPM_GET_CODEC_INFO_PARAMETERS
targetos: Windows
req.typenames: OPM_GET_CODEC_INFO_PARAMETERS
req.redist: 
ms.custom: 19H1
---

# OPM_GET_CODEC_INFO_PARAMETERS structure


## -description


Contains information for the <a href="https://docs.microsoft.com/windows/desktop/medfound/opm-get-codec-info">OPM_GET_CODEC_INFO</a> command.


## -struct-fields




### -field cbVerifier

The amount of valid data in the <b>Verifier</b> array, in bytes.


### -field Verifier

A byte array that contains one of the following:

<ul>
<li>The CLSID of the Media Foundation transform (MFT) that represents the hardware codec.</li>
<li>A null-terminated, wide-character string that contains the symbolic link for the hardware codec. Include the size of the terminating null in the value of the <b>cbVerifier</b> member. </li>
</ul>

## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/opm-structures">OPM Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a>
 

 

