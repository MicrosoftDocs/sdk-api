---
UID: NE:appmodel.AppPolicyThreadInitializationType
title: AppPolicyThreadInitializationType
author: windows-sdk-content
description: The AppPolicyThreadInitializationType enumeration indicates the kind of initialization that should be automatically performed for a process when beginthread[ex] creates a thread.
old-location: appxpkg\apppolicythreadinitializationtype_enumeration.htm
old-project: appxpkg
ms.assetid: F31AC156-5C27-4707-898A-3C8125E11FB3
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: AppPolicyThreadInitializationType, AppPolicyThreadInitializationType enumeration [App packaging and management], AppPolicyThreadInitializationType_InitializeWinRT, AppPolicyThreadInitializationType_None, appmodel/AppPolicyThreadInitializationType, appmodel/AppPolicyThreadInitializationType_InitializeWinRT, appmodel/AppPolicyThreadInitializationType_None, appxpkg.apppolicythreadinitializationtype_enumeration
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: AppPolicyThreadInitializationType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AppModel.h
api_name:
 - AppPolicyThreadInitializationType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# AppPolicyThreadInitializationType enumeration


## -description


The AppPolicyThreadInitializationType enumeration indicates the kind of initialization that should be automatically performed for a process when beginthread[ex] creates a thread.


## -enum-fields




### -field AppPolicyThreadInitializationType_None

Indicates that no initialization should be performed.


### -field AppPolicyThreadInitializationType_InitializeWinRT

Indicates that Windows Runtime initialization should be performed.

