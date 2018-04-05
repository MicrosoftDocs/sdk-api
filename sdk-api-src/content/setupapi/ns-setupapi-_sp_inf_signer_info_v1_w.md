---
UID: NS:setupapi._SP_INF_SIGNER_INFO_V1_W
title: "_SP_INF_SIGNER_INFO_V1_W"
author: windows-driver-content
description: The SP_INF_SIGNER_INFO structure stores information about an INF file's digital signature.
old-location: setup\sp_inf_signer_info.htm
old-project: SetupApi
ms.assetid: 50ceee47-3a89-4bd7-8508-5a4d75514861
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PSP_INF_SIGNER_INFO_V1_W, PSP_INF_SIGNER_INFO, PSP_INF_SIGNER_INFO structure pointer [Setup API], SP_INF_SIGNER_INFO, SP_INF_SIGNER_INFO structure [Setup API], SP_INF_SIGNER_INFO_V1, SP_INF_SIGNER_INFO_V1_W, SP_INF_SIGNER_INFO_W, _SP_INF_SIGNER_INFO_V1_W, _setupapi_filepaths_signerinfo, setup.sp_inf_signer_info, setupapi/PSP_INF_SIGNER_INFO, setupapi/SP_INF_SIGNER_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: SP_INF_SIGNER_INFO_V1_W, *PSP_INF_SIGNER_INFO_V1_W
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Setupapi.h
api_name:
-	SP_INF_SIGNER_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _SP_INF_SIGNER_INFO_V1_W structure


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


## -see-also




<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

