---
UID: NS:setupapi._SP_ORIGINAL_FILE_INFO_W
title: SP_ORIGINAL_FILE_INFO_W (setupapi.h)
author: windows-sdk-content
description: The SP_ORIGINAL_FILE_INFO structure receives the original INF file name and catalog file information returned by SetupQueryInfOriginalFileInformation.
old-location: setup\sp_original_file_info.htm
tech.root: SetupApi
ms.assetid: 9ce09717-7f01-4044-ad6b-edd04a2445f5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PSP_ORIGINAL_FILE_INFO_W, PSP_ORIGINAL_FILE_INFO, PSP_ORIGINAL_FILE_INFO structure pointer [Setup API], SP_ORIGINAL_FILE_INFO, SP_ORIGINAL_FILE_INFO structure [Setup API], SP_ORIGINAL_FILE_INFO_W, _setupapi_sp_original_file_info, setup.sp_original_file_info, setupapi/PSP_ORIGINAL_FILE_INFO, setupapi/SP_ORIGINAL_FILE_INFO"
ms.topic: struct
f1_keywords: 
 - "setupapi/SP_ORIGINAL_FILE_INFO"
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
 - SP_ORIGINAL_FILE_INFO
product: Windows
targetos: Windows
req.typenames: SP_ORIGINAL_FILE_INFO_W, *PSP_ORIGINAL_FILE_INFO_W
req.redist: 
ms.custom: 19H1
---

# SP_ORIGINAL_FILE_INFO_W structure


## -description


The 
<b>SP_ORIGINAL_FILE_INFO</b> structure receives the original INF file name and catalog file information returned by 
<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupqueryinforiginalfileinformationa">SetupQueryInfOriginalFileInformation</a>.


## -struct-fields




### -field cbSize

Size of this structure, in bytes.


### -field OriginalInfName

Original file name of the INF file stored in array of size MAX_PATH.


### -field OriginalCatalogName

Catalog name of the INF file stored in array of size MAX_PATH.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SetupApi/overview">Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/SetupApi/structures--setup-api-">Structures</a>
 

 

