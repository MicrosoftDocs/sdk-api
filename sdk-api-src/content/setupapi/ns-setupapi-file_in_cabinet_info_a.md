---
UID: NS:setupapi._FILE_IN_CABINET_INFO_A
title: FILE_IN_CABINET_INFO_A (setupapi.h)
description: The FILE_IN_CABINET_INFO structure provides information about a file found in the cabinet.helpviewer_keywords: ["*PFILE_IN_CABINET_INFO_A","FILE_IN_CABINET_INFO","FILE_IN_CABINET_INFO structure [Setup API]","FILE_IN_CABINET_INFO_A","PFILE_IN_CABINET_INFO","PFILE_IN_CABINET_INFO structure pointer [Setup API]","_setupapi_file_in_cabinet_info_str","setup.file_in_cabinet_info_str","setupapi/FILE_IN_CABINET_INFO","setupapi/PFILE_IN_CABINET_INFO"]
old-location: setup\file_in_cabinet_info_str.htm
tech.root: SetupApi
ms.assetid: 071491a8-f305-4e53-b0d7-16f7c9606e99
ms.date: 12/05/2018
ms.keywords: '*PFILE_IN_CABINET_INFO_A, FILE_IN_CABINET_INFO, FILE_IN_CABINET_INFO structure [Setup API], FILE_IN_CABINET_INFO_A, PFILE_IN_CABINET_INFO, PFILE_IN_CABINET_INFO structure pointer [Setup API], _setupapi_file_in_cabinet_info_str, setup.file_in_cabinet_info_str, setupapi/FILE_IN_CABINET_INFO, setupapi/PFILE_IN_CABINET_INFO'
f1_keywords:
- setupapi/FILE_IN_CABINET_INFO
dev_langs:
- c++
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
- FILE_IN_CABINET_INFO - file_in_cabinet_info_a
targetos: Windows
req.typenames: FILE_IN_CABINET_INFO_A, *PFILE_IN_CABINET_INFO_A
req.redist: 
ms.custom: 19H1
---

# FILE_IN_CABINET_INFO_A structure


## -description


The 
<b>FILE_IN_CABINET_INFO</b> structure provides information about a file found in the cabinet. The 
<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupiteratecabineta">SetupIterateCabinet</a> function sends this structure as one of the parameters when it sends a 
<a href="https://docs.microsoft.com/windows/desktop/SetupApi/spfilenotify-fileincabinet">SPFILENOTIFY_FILEINCABINET</a> notification to the cabinet callback routine.


## -struct-fields




### -field NameInCabinet

File name as it exists within the cabinet file.


### -field FileSize

Uncompressed size of the file in the cabinet, in bytes.


### -field Win32Error

If an error occurs, this member is the <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a>. If no error has occurred, it is  NO_ERROR.


### -field DosDate

Date that the file was last saved.


### -field DosTime

MS-DOS time stamp of the file in the cabinet.


### -field DosAttribs

Attributes of the file in the cabinet.


### -field FullTargetName

Target path and file name.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-cabinet_info_a">CABINET_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/SetupApi/overview">Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/SetupApi/structures--setup-api-">Structures</a>
 

 

