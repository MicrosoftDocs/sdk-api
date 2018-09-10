---
UID: NE:appmodel.AppPolicyProcessTerminationMethod
title: AppPolicyProcessTerminationMethod
author: windows-sdk-content
description: The AppPolicyProcessTerminationMethod enumeration indicates the method used to end a process.
old-location: appxpkg\apppolicyprocessterminationmethod_enumeration.htm
tech.root: appxpkg
ms.assetid: 874B576A-1AB5-4712-BF04-0406E5FE4923
ms.author: windowssdkdev
ms.date: 08/16/2018
ms.keywords: AppPolicyProcessTerminationMethod, AppPolicyProcessTerminationMethod enumeration [App packaging and management], AppPolicyProcessTerminationMethod_ExitProcess, AppPolicyProcessTerminationMethod_TerminateProcess, appmodel/AppPolicyProcessTerminationMethod, appmodel/AppPolicyProcessTerminationMethod_ExitProcess, appmodel/AppPolicyProcessTerminationMethod_TerminateProcess, appxpkg.apppolicyprocessterminationmethod_enumeration
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AppModel.h
api_name:
 - AppPolicyProcessTerminationMethod
product: Windows
targetos: Windows
req.typenames: AppPolicyProcessTerminationMethod
req.redist: 
---

# AppPolicyProcessTerminationMethod enumeration


## -description


The AppPolicyProcessTerminationMethod enumeration indicates the method used to end a process.


## -enum-fields




### -field AppPolicyProcessTerminationMethod_ExitProcess

Allows DLLs to execute code at shutdown. This value is expected for a desktop application, or for a Desktop Bridge application.


### -field AppPolicyProcessTerminationMethod_TerminateProcess

Immediately ends the process. This value is expected for a UWP app.

