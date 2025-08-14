---
UID: NF:appmodel.AppPolicyGetMediaFoundationCodecLoading
title: AppPolicyGetMediaFoundationCodecLoading function (appmodel.h)
description: Retrieves a value indicating whether a process’s policy allows it to load non-Windows (third-party) plugins. You can use the value to decide whether or not to allow non-Windows (third-party) plugins.
helpviewer_keywords: ["AppPolicyGetMediaFoundationCodecLoading","AppPolicyGetMediaFoundationCodecLoading function [App packaging and management]","appmodel/AppPolicyGetMediaFoundationCodecLoading","appxpkg.apppolicygetmediafoundationcodecloading"]
old-location: appxpkg\apppolicygetmediafoundationcodecloading.htm
tech.root: appxpkg
ms.assetid: 59231147-0505-4353-AADE-D81701ECBAD5
ms.date: 12/05/2018
ms.keywords: AppPolicyGetMediaFoundationCodecLoading, AppPolicyGetMediaFoundationCodecLoading function [App packaging and management], appmodel/AppPolicyGetMediaFoundationCodecLoading, appxpkg.apppolicygetmediafoundationcodecloading
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
 - AppPolicyGetMediaFoundationCodecLoading
 - appmodel/AppPolicyGetMediaFoundationCodecLoading
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
 - AppPolicyGetMediaFoundationCodecLoading
---

# AppPolicyGetMediaFoundationCodecLoading function


## -description

Retrieves a value indicating whether a process’s policy allows it to load non-Windows (third-party) plugins. You can use the value to decide whether or not to allow non-Windows (third-party) plugins.

## -parameters

### -param processToken [in]

A handle that identifies the access token for a process.

### -param policy [out]

A pointer to a variable of the <a href="../appmodel/ne-appmodel-apppolicymediafoundationcodecloading.md">AppPolicyMediaFoundationCodecLoading</a> enumerated type. When the function returns successfully, the variable contains an enumerated constant value indicating the codec-loading policy of the identified process.

## -returns

If the function succeeds, the function returns ERROR_SUCCESS.

If no known codec-loading policy was found for the process token, the function raises a STATUS_ASSERTION_FAILURE exception and returns ERROR_NOT_FOUND.

If either processToken or policy are null, the function returns ERROR_INVALID_PARAMETER.

