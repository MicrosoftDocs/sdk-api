---
UID: NF:appmodel.AppPolicyGetWindowingModel
title: AppPolicyGetWindowingModel function (appmodel.h)
description: Retrieves a value indicating whether a process uses a CoreWindow-based, or a HWND-based, windowing model. You can use the value to decide how to register for window state change notifications (size changed, visibility changed, etc.).
helpviewer_keywords: ["AppPolicyGetWindowingModel","AppPolicyGetWindowingModel function [App packaging and management]","appmodel/AppPolicyGetWindowingModel","appxpkg.apppolicygetwindowingmodel_function"]
old-location: appxpkg\apppolicygetwindowingmodel_function.htm
tech.root: appxpkg
ms.assetid: AA1682F8-1DDD-48C3-B16A-6C89D28455E8
ms.date: 12/05/2018
ms.keywords: AppPolicyGetWindowingModel, AppPolicyGetWindowingModel function [App packaging and management], appmodel/AppPolicyGetWindowingModel, appxpkg.apppolicygetwindowingmodel_function
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
 - AppPolicyGetWindowingModel
 - appmodel/AppPolicyGetWindowingModel
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
 - AppPolicyGetWindowingModel
---

# AppPolicyGetWindowingModel function


## -description

Retrieves a value indicating whether a process uses a CoreWindow-based, or a HWND-based, windowing model. You can use the value to decide how to register for window state change notifications (size changed, visibility changed, etc.).

## -parameters

### -param processToken [in]

A handle that identifies the access token for a process.

### -param policy [out]

A pointer to a variable of the <a href="/windows/win32/api/appmodel/ne-appmodel-apppolicywindowingmodel">AppPolicyWindowingModel</a> enumerated type. When the function returns successfully, the variable contains an enumerated constant value indicating the windowing model of the identified process.

## -returns

If the function succeeds, the function returns ERROR_SUCCESS.

If no known windowing model policy was found for the process token, the function raises a STATUS_ASSERTION_FAILURE exception and returns ERROR_NOT_FOUND.

If either processToken or policy are null, the function returns ERROR_INVALID_PARAMETER.

