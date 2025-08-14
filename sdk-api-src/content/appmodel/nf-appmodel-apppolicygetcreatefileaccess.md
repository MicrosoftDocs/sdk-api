---
UID: NF:appmodel.AppPolicyGetCreateFileAccess
title: AppPolicyGetCreateFileAccess function (appmodel.h)
description: Retrieves a value indicating whether a process has full or restricted access to the IO devices (file, file stream, directory, physical disk, volume, console buffer, tape drive, communications resource, mailslot, and pipe).
helpviewer_keywords: ["AppPolicyGetCreateFileAccess","AppPolicyGetCreateFileAccess function [App packaging and management]","appmodel/AppPolicyGetCreateFileAccess","appxpkg.apppolicygetcreatefileaccess_function"]
old-location: appxpkg\apppolicygetcreatefileaccess_function.htm
tech.root: appxpkg
ms.assetid: 3AFFEAE5-CD49-458D-BBB8-AEC3A71566D1
ms.date: 12/05/2018
ms.keywords: AppPolicyGetCreateFileAccess, AppPolicyGetCreateFileAccess function [App packaging and management], appmodel/AppPolicyGetCreateFileAccess, appxpkg.apppolicygetcreatefileaccess_function
req.header: appmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OneCoreUap.lib
req.dll: Api-ms-win-appmodel-runtime-l1-1-2.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AppPolicyGetCreateFileAccess
 - appmodel/AppPolicyGetCreateFileAccess
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-appmodel-runtime-l1-1-7.dll
 - api-ms-win-appmodel-runtime-l1-1-6.dll
 - api-ms-win-appmodel-runtime-l1-1-5.dll
 - api-ms-win-appmodel-runtime-l1-1-4.dll
 - api-ms-win-appmodel-runtime-l1-1-3.dll
 - api-ms-win-appmodel-runtime-l1-1-2.dll
 - kernel32.dll
api_name:
 - AppPolicyGetCreateFileAccess
---

# AppPolicyGetCreateFileAccess function


## -description

Retrieves a value indicating whether a process has full or restricted access to the IO devices (file, file stream, directory, physical disk, volume, console buffer, tape drive, communications resource, mailslot, and pipe).

## -parameters

### -param processToken [in]

A handle that identifies the access token for a process.

### -param policy [out]

A pointer to a variable of the <a href="/windows/desktop/api/appmodel/ne-appmodel-apppolicycreatefileaccess">AppPolicyCreateFileAccess</a> enumerated type. When the function returns successfully, the variable contains an enumerated constant value indicating whether the process has full or restricted access to the IO devices.

## -returns

If the function succeeds, the function returns ERROR_SUCCESS.

If no known create file access policy was found for the process token, the function raises a STATUS_ASSERTION_FAILURE exception and returns ERROR_NOT_FOUND.

If either processToken or policy are null, the function returns ERROR_INVALID_PARAMETER.