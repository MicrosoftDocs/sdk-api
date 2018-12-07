---
UID: NF:appmodel.AppPolicyGetProcessTerminationMethod
title: AppPolicyGetProcessTerminationMethod function
author: windows-sdk-content
description: Retrieves the method used to end a process.
old-location: appxpkg\apppolicygetprocessterminationmethod_function.htm
tech.root: appxpkg
ms.assetid: 7278DF60-A656-4FEE-A5D1-8C159A0B076D
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AppPolicyGetProcessTerminationMethod, AppPolicyGetProcessTerminationMethod function [App packaging and management], appmodel/AppPolicyGetProcessTerminationMethod, appxpkg.apppolicygetprocessterminationmethod_function
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - AppPolicyGetProcessTerminationMethod
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AppPolicyGetProcessTerminationMethod function


## -description


Retrieves the method used to end a process.


## -parameters




### -param processToken [in]

A handle that identifies the access token for a process.


### -param policy [out]

A pointer to a variable of the <a href="https://msdn.microsoft.com/874B576A-1AB5-4712-BF04-0406E5FE4923">AppPolicyProcessTerminationMethod</a> enumerated type. When the function returns successfully, the variable contains a value indicating the method used to end the process.


## -returns



If the function succeeds, the function returns ERROR_SUCCESS.

If no known process termination policy was found for the process token, the function raises a STATUS_ASSERTION_FAILURE exception and returns ERROR_NOT_FOUND.

If either processToken or policy are null, the function returns ERROR_INVALID_PARAMETER.



