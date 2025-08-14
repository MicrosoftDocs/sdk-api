---
UID: NF:appmodel.AppPolicyGetThreadInitializationType
title: AppPolicyGetThreadInitializationType function (appmodel.h)
description: Retrieves the kind of initialization that should be automatically performed for a process when beginthread[ex] creates a thread.
helpviewer_keywords: ["AppPolicyGetThreadInitializationType","AppPolicyGetThreadInitializationType function [App packaging and management]","appmodel/AppPolicyGetThreadInitializationType","appxpkg.apppolicygetthreadinitializationtype_function"]
old-location: appxpkg\apppolicygetthreadinitializationtype_function.htm
tech.root: appxpkg
ms.assetid: E8D52FDB-CD62-407A-9F70-2825E0BF8523
ms.date: 12/05/2018
ms.keywords: AppPolicyGetThreadInitializationType, AppPolicyGetThreadInitializationType function [App packaging and management], appmodel/AppPolicyGetThreadInitializationType, appxpkg.apppolicygetthreadinitializationtype_function
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
 - AppPolicyGetThreadInitializationType
 - appmodel/AppPolicyGetThreadInitializationType
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
 - kernel.appcore.dll
 - kernel32.dll
 - kernelbase.dll
api_name:
 - AppPolicyGetThreadInitializationType
---

# AppPolicyGetThreadInitializationType function


## -description

Retrieves the kind of initialization that should be automatically performed for a process when beginthread[ex] creates a thread.

## -parameters

### -param processToken [in]

A handle that identifies the access token for a process.

### -param policy [out]

A pointer to a variable of the <a href="/windows/desktop/api/appmodel/ne-appmodel-apppolicythreadinitializationtype">AppPolicyThreadInitializationType</a> enumerated type. When the function returns successfully, the variable contains a value indicating the kind of initialization that should be automatically performed for the process when beginthread[ex] creates a thread.

## -returns

If the function succeeds, the function returns ERROR_SUCCESS.

If no known thread initialization policy was found for the process token, the function raises a STATUS_ASSERTION_FAILURE exception and returns ERROR_NOT_FOUND.

If either processToken or policy are null, the function returns ERROR_INVALID_PARAMETER.