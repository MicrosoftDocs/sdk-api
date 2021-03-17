---
UID: NE:appmodel.AppPolicyClrCompat
title: AppPolicyClrCompat (appmodel.h)
description: The AppPolicyClrCompat enumeration indicates the application type of a process so that you can determine whether to enable private reflection and/or make managed objects agile.
helpviewer_keywords: ["AppPolicyClrCompat","AppPolicyClrCompat enumeration [App packaging and management]","AppPolicyClrCompat_ClassicDesktop","AppPolicyClrCompat_Other","AppPolicyClrCompat_PackagedDesktop","AppPolicyClrCompat_Universal","appmodel/AppPolicyClrCompat","appmodel/AppPolicyClrCompat_ClassicDesktop","appmodel/AppPolicyClrCompat_Other","appmodel/AppPolicyClrCompat_PackagedDesktop","appmodel/AppPolicyClrCompat_Universal","appxpkg.apppolicyclrcompat"]
old-location: appxpkg\apppolicyclrcompat.htm
tech.root: appxpkg
ms.assetid: 2653340E-FCDD-41B7-B72C-F99C92920645
ms.date: 12/05/2018
ms.keywords: AppPolicyClrCompat, AppPolicyClrCompat enumeration [App packaging and management], AppPolicyClrCompat_ClassicDesktop, AppPolicyClrCompat_Other, AppPolicyClrCompat_PackagedDesktop, AppPolicyClrCompat_Universal, appmodel/AppPolicyClrCompat, appmodel/AppPolicyClrCompat_ClassicDesktop, appmodel/AppPolicyClrCompat_Other, appmodel/AppPolicyClrCompat_PackagedDesktop, appmodel/AppPolicyClrCompat_Universal, appxpkg.apppolicyclrcompat
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
req.typenames: AppPolicyClrCompat
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AppPolicyClrCompat
 - appmodel/AppPolicyClrCompat
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
 - AppPolicyClrCompat
---

# AppPolicyClrCompat enumeration


## -description

The AppPolicyClrCompat enumeration indicates the application type of a process so that you can determine whether to enable private reflection and/or make managed objects agile.

## -enum-fields

### -field AppPolicyClrCompat_Other

Indicates an application type other than the ones indicated by the other enumerated constants. The Common Language Runtime (CLR) should not be called by applications that are not Universal Windows Platform (UWP), Win32, nor Desktop Bridge.

### -field AppPolicyClrCompat_ClassicDesktop

Indicates a desktop/Win32 application, or an NT service. You can support private reflection on framework types.

### -field AppPolicyClrCompat_Universal

Indicates a Universal Windows Platform (UWP) application. You should disable private reflection on framework types, but you can support IAgileObject.

### -field AppPolicyClrCompat_PackagedDesktop

Indicates a Desktop Bridge application. You can support private reflection on framework types, and you can support IAgileObject.

