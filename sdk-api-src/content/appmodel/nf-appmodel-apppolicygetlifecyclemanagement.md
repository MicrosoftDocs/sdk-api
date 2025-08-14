---
UID: NF:appmodel.AppPolicyGetLifecycleManagement
title: AppPolicyGetLifecycleManagement function (appmodel.h)
description: Retrieves a value indicating whether a process can be suspended/resumed by the Process Lifecycle Manager (PLM).
helpviewer_keywords: ["AppPolicyGetLifecycleManagement","AppPolicyGetLifecycleManagement function [App packaging and management]","appmodel/AppPolicyGetLifecycleManagement","appxpkg.apppolicygetlifecyclemanagement_function"]
old-location: appxpkg\apppolicygetlifecyclemanagement_function.htm
tech.root: appxpkg
ms.assetid: FED6C183-7AA9-428F-8815-F6BC9844B360
ms.date: 12/05/2018
ms.keywords: AppPolicyGetLifecycleManagement, AppPolicyGetLifecycleManagement function [App packaging and management], appmodel/AppPolicyGetLifecycleManagement, appxpkg.apppolicygetlifecyclemanagement_function
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
 - AppPolicyGetLifecycleManagement
 - appmodel/AppPolicyGetLifecycleManagement
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
 - AppPolicyGetLifecycleManagement
---

# AppPolicyGetLifecycleManagement function


## -description

Retrieves a value indicating whether a process can be suspended/resumed by the Process Lifecycle Manager (PLM). You can use the value to decide whether to subscribe to relevant notifications from the PLM, or to register for a classic system suspend notification.

## -parameters

### -param processToken [in]

A handle that identifies the access token for a process.

### -param policy [out]

A pointer to a variable of the <a href="../appmodel/ne-appmodel-apppolicylifecyclemanagement.md">AppPolicyLifecycleManagement</a> enumerated type. When the function returns successfully, the variable contains an enumerated constant value indicating whether the identified process is lifecycle-managed or not.

## -returns

If the function succeeds, the function returns ERROR_SUCCESS.

If no known lifecycle management policy was found for the process token, the function raises a STATUS_ASSERTION_FAILURE exception and returns ERROR_NOT_FOUND.

If either processToken or policy are null, the function returns ERROR_INVALID_PARAMETER.

