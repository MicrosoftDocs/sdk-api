---
UID: NS:setupapi._SP_INF_SIGNER_INFO_V2_W
title: SP_INF_SIGNER_INFO_V2_W
author: windows-sdk-content
description: The SP_INF_SIGNER_INFO structure stores information about an INF file's digital signature.
old-location: setup\sp_inf_signer_info.htm
tech.root: SetupApi
ms.assetid: 50ceee47-3a89-4bd7-8508-5a4d75514861
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PSP_INF_SIGNER_INFO_V2_W, PSP_INF_SIGNER_INFO, PSP_INF_SIGNER_INFO structure pointer [Setup API], SP_INF_SIGNER_INFO, SP_INF_SIGNER_INFO structure [Setup API], SP_INF_SIGNER_INFO_V2, SP_INF_SIGNER_INFO_V2_W, SP_INF_SIGNER_INFO_W, _setupapi_filepaths_signerinfo, setup.sp_inf_signer_info, setupapi/PSP_INF_SIGNER_INFO, setupapi/SP_INF_SIGNER_INFO"
ms.topic: struct
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Setupapi.h
api_name:
 - SP_INF_SIGNER_INFO
product: Windows
targetos: Windows
req.typenames: SP_INF_SIGNER_INFO_V2_W, *PSP_INF_SIGNER_INFO_V2_W
req.redist: 
---

# SP_INF_SIGNER_INFO_V2_W structure


## -description


The <b>SP_INF_SIGNER_INFO</b> structure stores information about an INF file's digital signature.


## -struct-fields




### -field cbSize

Size of this structure, in bytes.


### -field CatalogFile

Path to the catalog file, stored in an array of maximum size MAX_PATH characters.  


### -field DigitalSigner

Path to the digital signer of the file, stored in an array of maximum size MAX_PATH characters.


### -field DigitalSignerVersion

Version of the digital signer, stored in an array of size MAX_PATH characters.


### -field SignerScore

 




## -see-also




<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/837F1864-CE2F-4A9A-A7D9-18EB8622541E">Structures</a>
 

 

