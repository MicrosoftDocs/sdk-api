---
UID: NS:setupapi._FILE_IN_CABINET_INFO_A
title: "_FILE_IN_CABINET_INFO_A"
author: windows-sdk-content
description: The FILE_IN_CABINET_INFO structure provides information about a file found in the cabinet.
old-location: setup\file_in_cabinet_info_str.htm
old-project: SetupApi
ms.assetid: 071491a8-f305-4e53-b0d7-16f7c9606e99
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: "*PFILE_IN_CABINET_INFO_A, FILE_IN_CABINET_INFO, FILE_IN_CABINET_INFO structure [Setup API], FILE_IN_CABINET_INFO_A, PFILE_IN_CABINET_INFO, PFILE_IN_CABINET_INFO structure pointer [Setup API], _FILE_IN_CABINET_INFO_A, _setupapi_file_in_cabinet_info_str, setup.file_in_cabinet_info_str, setupapi/FILE_IN_CABINET_INFO, setupapi/PFILE_IN_CABINET_INFO"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FILE_IN_CABINET_INFO_A, *PFILE_IN_CABINET_INFO_A
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Setupapi.h
api_name:
 - FILE_IN_CABINET_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _FILE_IN_CABINET_INFO_A structure


## -description


The 
<b>FILE_IN_CABINET_INFO</b> structure provides information about a file found in the cabinet. The 
<a href="https://msdn.microsoft.com/2fa2d140-fa8e-41a8-9800-d10e5559fab4">SetupIterateCabinet</a> function sends this structure as one of the parameters when it sends a 
<a href="https://msdn.microsoft.com/c6d89759-c0d4-4741-b992-43eaa0dc4f01">SPFILENOTIFY_FILEINCABINET</a> notification to the cabinet callback routine.


## -struct-fields




### -field NameInCabinet

File name as it exists within the cabinet file.


### -field FileSize

Uncompressed size of the file in the cabinet, in bytes.


### -field Win32Error

If an error occurs, this member is the <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. If no error has occurred, it is  NO_ERROR.


### -field DosDate

Date that the file was last saved.


### -field DosTime

MS-DOS time stamp of the file in the cabinet.


### -field DosAttribs

Attributes of the file in the cabinet.


### -field FullTargetName

Target path and file name.


## -see-also




<a href="https://msdn.microsoft.com/205bff19-d9ac-4dc0-ab11-92cf70a3bd49">CABINET_INFO</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

