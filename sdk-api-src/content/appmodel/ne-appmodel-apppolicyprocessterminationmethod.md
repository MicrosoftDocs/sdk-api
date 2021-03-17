---
UID: NE:appmodel.AppPolicyProcessTerminationMethod
title: AppPolicyProcessTerminationMethod (appmodel.h)
description: The AppPolicyProcessTerminationMethod enumeration indicates the method used to end a process.
helpviewer_keywords: ["AppPolicyProcessTerminationMethod","AppPolicyProcessTerminationMethod enumeration [App packaging and management]","AppPolicyProcessTerminationMethod_ExitProcess","AppPolicyProcessTerminationMethod_TerminateProcess","appmodel/AppPolicyProcessTerminationMethod","appmodel/AppPolicyProcessTerminationMethod_ExitProcess","appmodel/AppPolicyProcessTerminationMethod_TerminateProcess","appxpkg.apppolicyprocessterminationmethod_enumeration"]
old-location: appxpkg\apppolicyprocessterminationmethod_enumeration.htm
tech.root: appxpkg
ms.assetid: 874B576A-1AB5-4712-BF04-0406E5FE4923
ms.date: 12/05/2018
ms.keywords: AppPolicyProcessTerminationMethod, AppPolicyProcessTerminationMethod enumeration [App packaging and management], AppPolicyProcessTerminationMethod_ExitProcess, AppPolicyProcessTerminationMethod_TerminateProcess, appmodel/AppPolicyProcessTerminationMethod, appmodel/AppPolicyProcessTerminationMethod_ExitProcess, appmodel/AppPolicyProcessTerminationMethod_TerminateProcess, appxpkg.apppolicyprocessterminationmethod_enumeration
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
req.typenames: AppPolicyProcessTerminationMethod
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AppPolicyProcessTerminationMethod
 - appmodel/AppPolicyProcessTerminationMethod
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
 - AppPolicyProcessTerminationMethod
---

# AppPolicyProcessTerminationMethod enumeration


## -description

The AppPolicyProcessTerminationMethod enumeration indicates the method used to end a process.

## -enum-fields

### -field AppPolicyProcessTerminationMethod_ExitProcess

Allows DLLs to execute code at shutdown. This value is expected for a desktop application, or for a Desktop Bridge application.

### -field AppPolicyProcessTerminationMethod_TerminateProcess

Immediately ends the process. This value is expected for a UWP app.

