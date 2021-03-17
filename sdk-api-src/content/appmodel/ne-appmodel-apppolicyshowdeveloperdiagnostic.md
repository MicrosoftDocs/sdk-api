---
UID: NE:appmodel.AppPolicyShowDeveloperDiagnostic
title: AppPolicyShowDeveloperDiagnostic (appmodel.h)
description: The AppPolicyShowDeveloperDiagnostic enumeration indicates the method used for a process to surface developer information, such as asserts, to the user.
helpviewer_keywords: ["AppPolicyShowDeveloperDiagnostic","AppPolicyShowDeveloperDiagnostic enumeration [App packaging and management]","AppPolicyShowDeveloperDiagnostic_None","AppPolicyShowDeveloperDiagnostic_ShowUI","appmodel/AppPolicyShowDeveloperDiagnostic","appmodel/AppPolicyShowDeveloperDiagnostic_None","appmodel/AppPolicyShowDeveloperDiagnostic_ShowUI","appxpkg.apppolicyshowdeveloperdiagnostic_enumeration"]
old-location: appxpkg\apppolicyshowdeveloperdiagnostic_enumeration.htm
tech.root: appxpkg
ms.assetid: 4D8E137C-AD50-45E6-9284-98904021678A
ms.date: 12/05/2018
ms.keywords: AppPolicyShowDeveloperDiagnostic, AppPolicyShowDeveloperDiagnostic enumeration [App packaging and management], AppPolicyShowDeveloperDiagnostic_None, AppPolicyShowDeveloperDiagnostic_ShowUI, appmodel/AppPolicyShowDeveloperDiagnostic, appmodel/AppPolicyShowDeveloperDiagnostic_None, appmodel/AppPolicyShowDeveloperDiagnostic_ShowUI, appxpkg.apppolicyshowdeveloperdiagnostic_enumeration
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
req.typenames: AppPolicyShowDeveloperDiagnostic
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AppPolicyShowDeveloperDiagnostic
 - appmodel/AppPolicyShowDeveloperDiagnostic
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
 - AppPolicyShowDeveloperDiagnostic
---

# AppPolicyShowDeveloperDiagnostic enumeration


## -description

The AppPolicyShowDeveloperDiagnostic enumeration indicates the method used for a process to surface developer information, such as asserts, to the user.

## -enum-fields

### -field AppPolicyShowDeveloperDiagnostic_None

Indicates that the process does not show developer diagnostics. This value is expected for a UWP app.

### -field AppPolicyShowDeveloperDiagnostic_ShowUI

Indicates that the process shows developer diagnostics UI. This value is expected for a desktop application, or for a Desktop Bridge application.

