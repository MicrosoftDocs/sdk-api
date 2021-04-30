---
UID: NE:appmodel.AppPolicyThreadInitializationType
title: AppPolicyThreadInitializationType (appmodel.h)
description: The AppPolicyThreadInitializationType enumeration indicates the kind of initialization that should be automatically performed for a process when beginthread[ex] creates a thread.
helpviewer_keywords: ["AppPolicyThreadInitializationType","AppPolicyThreadInitializationType enumeration [App packaging and management]","AppPolicyThreadInitializationType_InitializeWinRT","AppPolicyThreadInitializationType_None","appmodel/AppPolicyThreadInitializationType","appmodel/AppPolicyThreadInitializationType_InitializeWinRT","appmodel/AppPolicyThreadInitializationType_None","appxpkg.apppolicythreadinitializationtype_enumeration"]
old-location: appxpkg\apppolicythreadinitializationtype_enumeration.htm
tech.root: appxpkg
ms.assetid: F31AC156-5C27-4707-898A-3C8125E11FB3
ms.date: 12/05/2018
ms.keywords: AppPolicyThreadInitializationType, AppPolicyThreadInitializationType enumeration [App packaging and management], AppPolicyThreadInitializationType_InitializeWinRT, AppPolicyThreadInitializationType_None, appmodel/AppPolicyThreadInitializationType, appmodel/AppPolicyThreadInitializationType_InitializeWinRT, appmodel/AppPolicyThreadInitializationType_None, appxpkg.apppolicythreadinitializationtype_enumeration
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: AppPolicyThreadInitializationType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AppPolicyThreadInitializationType
 - appmodel/AppPolicyThreadInitializationType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AppModel.h
api_name:
 - AppPolicyThreadInitializationType
---

# AppPolicyThreadInitializationType enumeration


## -description

The AppPolicyThreadInitializationType enumeration indicates the kind of initialization that should be automatically performed for a process when beginthread[ex] creates a thread.

## -enum-fields

### -field AppPolicyThreadInitializationType_None

Indicates that no initialization should be performed.

### -field AppPolicyThreadInitializationType_InitializeWinRT

Indicates that Windows Runtime initialization should be performed.

