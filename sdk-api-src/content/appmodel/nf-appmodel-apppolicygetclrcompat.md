---
UID: NF:appmodel.AppPolicyGetClrCompat
title: AppPolicyGetClrCompat function (appmodel.h)
description: Retrieves a value indicating the application type of a process so that you can determine whether to enable private reflection and/or make managed objects agile.
helpviewer_keywords: ["AppPolicyGetClrCompat","AppPolicyGetClrCompat function [App packaging and management]","appmodel/AppPolicyGetClrCompat","appxpkg.apppolicygetclrcompat"]
old-location: appxpkg\apppolicygetclrcompat.htm
tech.root: appxpkg
ms.assetid: FCB15725-CA80-4C4E-9592-D69E0C937DB4
ms.date: 12/05/2018
ms.keywords: AppPolicyGetClrCompat, AppPolicyGetClrCompat function [App packaging and management], appmodel/AppPolicyGetClrCompat, appxpkg.apppolicygetclrcompat
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
 - AppPolicyGetClrCompat
 - appmodel/AppPolicyGetClrCompat
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
api_name:
 - AppPolicyGetClrCompat
---

# AppPolicyGetClrCompat function


## -description

Retrieves a value indicating the application type of a process so that you can determine whether to enable private reflection and/or make managed objects agile.

## -parameters

### -param processToken [in]

A handle that identifies the access token for a process.

### -param policy [out]

A pointer to a variable of the <a href="../appmodel/ne-appmodel-apppolicyclrcompat.md">AppPolicyClrCompat</a> enumerated type. When the function returns successfully, the variable contains an enumerated constant value indicating the application type of the identified process.

## -returns

If the function succeeds, the function returns ERROR_SUCCESS.

If no known application type was found for the process token, the function raises a STATUS_ASSERTION_FAILURE exception and returns ERROR_NOT_FOUND.

If either processToken or policy are null, the function returns ERROR_INVALID_PARAMETER.

