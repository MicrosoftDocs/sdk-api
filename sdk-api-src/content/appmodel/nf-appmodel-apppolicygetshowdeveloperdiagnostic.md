---
UID: NF:appmodel.AppPolicyGetShowDeveloperDiagnostic
title: AppPolicyGetShowDeveloperDiagnostic function (appmodel.h)
description: Retrieves the method used for a process to surface developer information, such as asserts, to the user.
helpviewer_keywords: ["AppPolicyGetShowDeveloperDiagnostic","AppPolicyGetShowDeveloperDiagnostic function [App packaging and management]","appmodel/AppPolicyGetShowDeveloperDiagnostic","appxpkg.apppolicygetshowdeveloperdiagnostic_function"]
old-location: appxpkg\apppolicygetshowdeveloperdiagnostic_function.htm
tech.root: appxpkg
ms.assetid: A6F794BE-7F40-4216-9E26-63D06B57FDD1
ms.date: 12/05/2018
ms.keywords: AppPolicyGetShowDeveloperDiagnostic, AppPolicyGetShowDeveloperDiagnostic function [App packaging and management], appmodel/AppPolicyGetShowDeveloperDiagnostic, appxpkg.apppolicygetshowdeveloperdiagnostic_function
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
 - AppPolicyGetShowDeveloperDiagnostic
 - appmodel/AppPolicyGetShowDeveloperDiagnostic
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
 - AppPolicyGetShowDeveloperDiagnostic
---

# AppPolicyGetShowDeveloperDiagnostic function


## -description

Retrieves the method used for a process to surface developer information, such as asserts, to the user.

## -parameters

### -param processToken [in]

A handle that identifies the access token for a process.

### -param policy [out]

A pointer to a variable of the <a href="/windows/desktop/api/appmodel/ne-appmodel-apppolicyshowdeveloperdiagnostic">AppPolicyShowDeveloperDiagnostic</a> enumerated type. When the function returns successfully, the variable contains a value indicating the method used for the process to surface developer information, such as asserts, to the user.

## -returns

If the function succeeds, the function returns ERROR_SUCCESS.

If no known developer information  policy was found for the process token, the function raises a STATUS_ASSERTION_FAILURE exception and returns ERROR_NOT_FOUND.

If either processToken or policy are null, the function returns ERROR_INVALID_PARAMETER.