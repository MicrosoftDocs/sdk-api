---
UID: NE:appmodel.AppPolicyWindowingModel
title: AppPolicyWindowingModel (appmodel.h)
description: The AppPolicyWindowingModel enumeration indicates whether a process uses a CoreWindow-based, or a HWND-based, windowing model.
helpviewer_keywords: ["AppPolicyWindowingModel","AppPolicyWindowingModel enumeration [App packaging and management]","AppPolicyWindowingModel_ClassicDesktop","AppPolicyWindowingModel_ClassicPhone","AppPolicyWindowingModel_None","AppPolicyWindowingModel_Universal","appmodel/AppPolicyWindowingModel","appmodel/AppPolicyWindowingModel_ClassicDesktop","appmodel/AppPolicyWindowingModel_ClassicPhone","appmodel/AppPolicyWindowingModel_None","appmodel/AppPolicyWindowingModel_Universal","appxpkg.apppolicywindowingmodel_enumeration"]
old-location: appxpkg\apppolicywindowingmodel_enumeration.htm
tech.root: appxpkg
ms.assetid: 236BCD35-6778-43A4-8B5E-59E9A49002FA
ms.date: 12/05/2018
ms.keywords: AppPolicyWindowingModel, AppPolicyWindowingModel enumeration [App packaging and management], AppPolicyWindowingModel_ClassicDesktop, AppPolicyWindowingModel_ClassicPhone, AppPolicyWindowingModel_None, AppPolicyWindowingModel_Universal, appmodel/AppPolicyWindowingModel, appmodel/AppPolicyWindowingModel_ClassicDesktop, appmodel/AppPolicyWindowingModel_ClassicPhone, appmodel/AppPolicyWindowingModel_None, appmodel/AppPolicyWindowingModel_Universal, appxpkg.apppolicywindowingmodel_enumeration
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
req.typenames: AppPolicyWindowingModel
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AppPolicyWindowingModel
 - appmodel/AppPolicyWindowingModel
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
 - AppPolicyWindowingModel
---

# AppPolicyWindowingModel enumeration


## -description

The AppPolicyWindowingModel enumeration indicates whether a process uses a CoreWindow-based, or a HWND-based, windowing model.

## -enum-fields

### -field AppPolicyWindowingModel_None

Indicates that the process doesn't have a windowing model.

### -field AppPolicyWindowingModel_Universal

Indicates that the process's windowing model is CoreWindow-based.

### -field AppPolicyWindowingModel_ClassicDesktop

Indicates that the process's windowing model is HWND-based.

### -field AppPolicyWindowingModel_ClassicPhone

Indicates that the process's windowing model is Silverlight-based, and does not provide notifications for window state changes.

