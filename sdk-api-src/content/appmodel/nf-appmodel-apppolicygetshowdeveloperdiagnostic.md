---
UID: NF:appmodel.AppPolicyGetShowDeveloperDiagnostic
title: AppPolicyGetShowDeveloperDiagnostic function (appmodel.h)
author: windows-sdk-content
description: Retrieves the method used for a process to surface developer information, such as asserts, to the user.
old-location: appxpkg\apppolicygetshowdeveloperdiagnostic_function.htm
tech.root: appxpkg
ms.assetid: A6F794BE-7F40-4216-9E26-63D06B57FDD1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AppPolicyGetShowDeveloperDiagnostic, AppPolicyGetShowDeveloperDiagnostic function [App packaging and management], appmodel/AppPolicyGetShowDeveloperDiagnostic, appxpkg.apppolicygetshowdeveloperdiagnostic_function
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-appmodel-runtime-l1-1-2.dll
 - kernel.appcore.dll
 - kernel32.dll
 - kernelbase.dll
api_name:
 - AppPolicyGetShowDeveloperDiagnostic
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AppPolicyGetShowDeveloperDiagnostic function


## -description


Retrieves the method used for a process to surface developer information, such as asserts, to the user.


## -parameters




### -param processToken [in]

A handle that identifies the access token for a process.


### -param policy [out]

A pointer to a variable of the <a href="https://msdn.microsoft.com/4D8E137C-AD50-45E6-9284-98904021678A">AppPolicyShowDeveloperDiagnostic</a> enumerated type. When the function returns successfully, the variable contains a value indicating the method used for the process to surface developer information, such as asserts, to the user.


## -returns



If the function succeeds, the function returns ERROR_SUCCESS.

If no known developer information  policy was found for the process token, the function raises a STATUS_ASSERTION_FAILURE exception and returns ERROR_NOT_FOUND.

If either processToken or policy are null, the function returns ERROR_INVALID_PARAMETER.



