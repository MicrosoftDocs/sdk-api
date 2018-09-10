---
UID: NF:appmodel.AppPolicyGetClrCompat
title: AppPolicyGetClrCompat function
author: windows-sdk-content
description: Retrieves a value indicating the application type of a process so that you can determine whether to enable private reflection and/or make managed objects agile.
old-location: appxpkg\apppolicygetclrcompat.htm
tech.root: appxpkg
ms.assetid: FCB15725-CA80-4C4E-9592-D69E0C937DB4
ms.author: windowssdkdev
ms.date: 08/16/2018
ms.keywords: AppPolicyGetClrCompat, AppPolicyGetClrCompat function [App packaging and management], appmodel/AppPolicyGetClrCompat, appxpkg.apppolicygetclrcompat
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
api_name:
 - AppPolicyGetClrCompat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AppPolicyGetClrCompat function


## -description


Retrieves a value indicating the application type of a process so that you can determine whether to enable private reflection and/or make managed objects agile.


## -parameters




### -param processToken [in]

A handle that identifies the access token for a process.


### -param policy [out]

A pointer to a variable of the <a href="https://msdn.microsoft.com/2653340E-FCDD-41B7-B72C-F99C92920645">AppPolicyClrCompat</a> enumerated type. When the function returns successfully, the variable contains an enumerated constant value indicating the application type of the identified process.


## -returns



If the function succeeds, the function returns ERROR_SUCCESS.

If no known application type was found for the process token, the function raises a STATUS_ASSERTION_FAILURE exception and returns ERROR_NOT_FOUND.

If either processToken or policy are null, the function returns ERROR_INVALID_PARAMETER.



