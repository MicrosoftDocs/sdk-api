---
UID: NS:opmapi._OPM_GET_CODEC_INFO_INFORMATION
title: "_OPM_GET_CODEC_INFO_INFORMATION"
author: windows-sdk-content
description: Contains the result from an OPM_GET_CODEC_INFO query.
old-location: mf\opm_get_codec_info_information.htm
tech.root: medfound
ms.assetid: 20865210-7f0f-4310-879e-9d1fe97f5df2
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: OPM_GET_CODEC_INFO_INFORMATION, OPM_GET_CODEC_INFO_INFORMATION structure [Media Foundation], _OPM_GET_CODEC_INFO_INFORMATION, ksopmapi/OPM_GET_CODEC_INFO_INFORMATION, mf.opm_get_codec_info_information
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: OPM_GET_CODEC_INFO_INFORMATION
req.redist: 
---

# _OPM_GET_CODEC_INFO_INFORMATION structure


## -description


Contains the result from an <a href="https://msdn.microsoft.com/51987a79-78bf-41b2-8349-8c2725dd89d6">OPM_GET_CODEC_INFO</a> query.


## -struct-fields




### -field rnRandomNumber

An <a href="https://msdn.microsoft.com/d3a5be4b-39d1-43da-b87e-ab4dd7815262">OPM_RANDOM_NUMBER</a> structure. This structure contains the same 128-bit random number that the application sent to the driver in the <a href="https://msdn.microsoft.com/8959c7d1-9a78-497f-8841-d3e61e9db6a3">OPM_GET_INFO_PARAMETERS</a> structure.


### -field Merit

The merit value of the codec.


## -see-also




<a href="https://msdn.microsoft.com/676a60ca-393e-4b5d-89d3-50cf4b771492">OPM Structures</a>



<a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a>
 

 

