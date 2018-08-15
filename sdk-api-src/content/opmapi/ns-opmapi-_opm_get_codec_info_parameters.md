---
UID: NS:opmapi._OPM_GET_CODEC_INFO_PARAMETERS
title: "_OPM_GET_CODEC_INFO_PARAMETERS"
author: windows-sdk-content
description: Contains information for the OPM_GET_CODEC_INFO command.
old-location: mf\opm_get_codec_info_parameters.htm
old-project: medfound
ms.assetid: 9fb130e5-fd87-4a11-9c9e-7a106a091b35
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: OPM_GET_CODEC_INFO_PARAMETERS, OPM_GET_CODEC_INFO_PARAMETERS structure [Media Foundation], _OPM_GET_CODEC_INFO_PARAMETERS, ksopmapi/OPM_GET_CODEC_INFO_PARAMETERS, mf.opm_get_codec_info_parameters
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: opmapi.h
req.include-header: Opmapi.h
req.redist: 
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
tech.root: 
req.typenames: OPM_GET_CODEC_INFO_PARAMETERS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ksopmapi.h
api_name:
 - OPM_GET_CODEC_INFO_PARAMETERS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _OPM_GET_CODEC_INFO_PARAMETERS structure


## -description


Contains information for the <a href="https://msdn.microsoft.com/51987a79-78bf-41b2-8349-8c2725dd89d6">OPM_GET_CODEC_INFO</a> command.


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




<a href="https://msdn.microsoft.com/676a60ca-393e-4b5d-89d3-50cf4b771492">OPM Structures</a>



<a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a>
 

 

