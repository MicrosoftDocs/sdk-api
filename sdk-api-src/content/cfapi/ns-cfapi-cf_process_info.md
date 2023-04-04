---
UID: NS:cfapi.CF_PROCESS_INFO
title: CF_PROCESS_INFO (cfapi.h)
description: Contains information about a user process.
helpviewer_keywords: ["CF_PROCESS_INFO","CF_PROCESS_INFO structure","cfapi/CF_PROCESS_INFO","cloudApi.cf_process_info"]
old-location: cloudapi\cf_process_info.htm
tech.root: cloudapi
ms.assetid: 912433E9-DC49-41BA-85F7-1A0AF9F88159
ms.date: 04/04/2023
ms.keywords: CF_PROCESS_INFO, CF_PROCESS_INFO structure, cfapi/CF_PROCESS_INFO, cloudApi.cf_process_info
req.header: cfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: CF_PROCESS_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_PROCESS_INFO
 - cfapi/CF_PROCESS_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CfApi.h
api_name:
 - CF_PROCESS_INFO
---

# CF_PROCESS_INFO structure

## -description

Contains information about a user process that triggers a callback.

## -struct-fields

### -field StructSize

The size of the **CF_PROCESS_INFO** structure.

### -field ProcessId

The 32 bit ID of the user process.

### -field ImagePath

The absolute path of the main executable file including the volume name in the format of NT file path. If the platform failed to retrieve the image path, `UNKNOWN` will be returned.

### -field PackageName

Used for modern applications. The app package name.

### -field ApplicationId

Used for modern applications. The application ID.

### -field CommandLine

>[!NOTE]
>This member was added in Windows 10, version 1803.

The string that is used to start the process. If the platform failed to retrieve the command line, `UNKNOWN` will be returned.

### -field SessionId

>[!NOTE]
>This member was added in Windows 10, version 1803.

The 32bit ID of the session wherein the user process that triggers the callback resides.

## -see-also

[CF_CALLBACK_INFO](ns-cfapi-cf_callback_info.md)
