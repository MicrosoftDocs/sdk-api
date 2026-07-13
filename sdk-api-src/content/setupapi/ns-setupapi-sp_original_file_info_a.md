---
UID: NS:setupapi._SP_ORIGINAL_FILE_INFO_A
title: SP_ORIGINAL_FILE_INFO_A (setupapi.h)
description: The SP_ORIGINAL_FILE_INFO structure receives the original INF file name and catalog file information returned by SetupQueryInfOriginalFileInformation. (ANSI)
helpviewer_keywords: ["*PSP_ORIGINAL_FILE_INFO_A","PSP_ORIGINAL_FILE_INFO","PSP_ORIGINAL_FILE_INFO structure pointer [Setup API]","SP_ORIGINAL_FILE_INFO","SP_ORIGINAL_FILE_INFO structure [Setup API]","SP_ORIGINAL_FILE_INFO_A","_setupapi_sp_original_file_info","setup.sp_original_file_info","setupapi/PSP_ORIGINAL_FILE_INFO","setupapi/SP_ORIGINAL_FILE_INFO"]
old-location: setup\sp_original_file_info.htm
tech.root: setup
ms.assetid: 9ce09717-7f01-4044-ad6b-edd04a2445f5
ms.date: 12/05/2018
ms.keywords: '*PSP_ORIGINAL_FILE_INFO_A, PSP_ORIGINAL_FILE_INFO, PSP_ORIGINAL_FILE_INFO structure pointer [Setup API], SP_ORIGINAL_FILE_INFO, SP_ORIGINAL_FILE_INFO structure [Setup API], SP_ORIGINAL_FILE_INFO_A, _setupapi_sp_original_file_info, setup.sp_original_file_info, setupapi/PSP_ORIGINAL_FILE_INFO, setupapi/SP_ORIGINAL_FILE_INFO'
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
req.typenames: SP_ORIGINAL_FILE_INFO_A, *PSP_ORIGINAL_FILE_INFO_A
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SP_ORIGINAL_FILE_INFO_A
 - setupapi/_SP_ORIGINAL_FILE_INFO_A
 - PSP_ORIGINAL_FILE_INFO_A
 - setupapi/PSP_ORIGINAL_FILE_INFO_A
 - SP_ORIGINAL_FILE_INFO_A
 - setupapi/SP_ORIGINAL_FILE_INFO_A
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
 - SP_ORIGINAL_FILE_INFO
 - sp_original_file_info_a
---

# SP_ORIGINAL_FILE_INFO_A structure


## -description

The 
<b>SP_ORIGINAL_FILE_INFO</b> structure receives the original INF file name and catalog file information returned by 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupqueryinforiginalfileinformationa">SetupQueryInfOriginalFileInformation</a>.

## -struct-fields

### -field cbSize

Size of this structure, in bytes.

### -field OriginalInfName

Original file name of the INF file stored in array of size MAX_PATH.

### -field OriginalCatalogName

Catalog name of the INF file stored in array of size MAX_PATH.

## -see-also

<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/SetupApi/structures--setup-api-">Structures</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines SP_ORIGINAL_FILE_INFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
