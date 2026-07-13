---
UID: NS:setupapi._SP_INF_SIGNER_INFO_V2_W
title: SP_INF_SIGNER_INFO_V2_W (setupapi.h)
description: The SP_INF_SIGNER_INFO structure stores information about an INF file's digital signature. (sp_inf_signer_info_v2_w)
helpviewer_keywords: ["*PSP_INF_SIGNER_INFO_V2_W","PSP_INF_SIGNER_INFO","PSP_INF_SIGNER_INFO structure pointer [Setup API]","SP_INF_SIGNER_INFO","SP_INF_SIGNER_INFO structure [Setup API]","SP_INF_SIGNER_INFO_V2","SP_INF_SIGNER_INFO_V2_W","SP_INF_SIGNER_INFO_W","_setupapi_filepaths_signerinfo","setup.sp_inf_signer_info","setupapi/PSP_INF_SIGNER_INFO","setupapi/SP_INF_SIGNER_INFO"]
old-location: setup\sp_inf_signer_info.htm
tech.root: setup
ms.assetid: 50ceee47-3a89-4bd7-8508-5a4d75514861
ms.date: 12/05/2018
ms.keywords: '*PSP_INF_SIGNER_INFO_V2_W, PSP_INF_SIGNER_INFO, PSP_INF_SIGNER_INFO structure pointer [Setup API], SP_INF_SIGNER_INFO, SP_INF_SIGNER_INFO structure [Setup API], SP_INF_SIGNER_INFO_V2, SP_INF_SIGNER_INFO_V2_W, SP_INF_SIGNER_INFO_W, _setupapi_filepaths_signerinfo, setup.sp_inf_signer_info, setupapi/PSP_INF_SIGNER_INFO, setupapi/SP_INF_SIGNER_INFO'
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
targetos: Windows
req.typenames: SP_INF_SIGNER_INFO_V2_W, *PSP_INF_SIGNER_INFO_V2_W
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SP_INF_SIGNER_INFO_V2_W
 - setupapi/_SP_INF_SIGNER_INFO_V2_W
 - PSP_INF_SIGNER_INFO_V2_W
 - setupapi/PSP_INF_SIGNER_INFO_V2_W
 - SP_INF_SIGNER_INFO_V2_W
 - setupapi/SP_INF_SIGNER_INFO_V2_W
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Setupapi.h
api_name:
 - SP_INF_SIGNER_INFO
 - sp_inf_signer_info_v2_w
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

<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/SetupApi/structures--setup-api-">Structures</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines SP_INF_SIGNER_INFO_V2 as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
