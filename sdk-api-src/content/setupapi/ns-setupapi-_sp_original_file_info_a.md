---
UID: NS:setupapi._SP_ORIGINAL_FILE_INFO_A
title: "_SP_ORIGINAL_FILE_INFO_A"
author: windows-driver-content
description: The SP_ORIGINAL_FILE_INFO structure receives the original INF file name and catalog file information returned by SetupQueryInfOriginalFileInformation.
old-location: setup\sp_original_file_info.htm
old-project: SetupApi
ms.assetid: 9ce09717-7f01-4044-ad6b-edd04a2445f5
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: "*PSP_ORIGINAL_FILE_INFO_A, PSP_ORIGINAL_FILE_INFO, PSP_ORIGINAL_FILE_INFO structure pointer [Setup API], SP_ORIGINAL_FILE_INFO, SP_ORIGINAL_FILE_INFO structure [Setup API], SP_ORIGINAL_FILE_INFO_A, _SP_ORIGINAL_FILE_INFO_A, _setupapi_sp_original_file_info, setup.sp_original_file_info, setupapi/PSP_ORIGINAL_FILE_INFO, setupapi/SP_ORIGINAL_FILE_INFO"
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
req.typenames: SP_ORIGINAL_FILE_INFO_A, *PSP_ORIGINAL_FILE_INFO_A
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Setupapi.h
api_name:
-	SP_ORIGINAL_FILE_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _SP_ORIGINAL_FILE_INFO_A structure


## -description


The 
<b>SP_ORIGINAL_FILE_INFO</b> structure receives the original INF file name and catalog file information returned by 
<a href="https://msdn.microsoft.com/bc7c08ff-3d6b-4d45-b634-1358302f6fc6">SetupQueryInfOriginalFileInformation</a>.


## -struct-fields




### -field cbSize

Size of this structure, in bytes.


### -field OriginalInfName

Original file name of the INF file stored in array of size MAX_PATH.


### -field OriginalCatalogName

Catalog name of the INF file stored in array of size MAX_PATH.


## -see-also




<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

