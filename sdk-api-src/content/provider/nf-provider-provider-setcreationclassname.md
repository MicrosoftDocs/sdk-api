---
UID: NF:provider.Provider.SetCreationClassName
title: Provider::SetCreationClassName (provider.h)
description: The SetCreationClassName method sets the CreationClassName string property, if any, of the given instance to the name of this provider.
helpviewer_keywords: ["Provider interface [Windows Management Instrumentation]","SetCreationClassName method","Provider.SetCreationClassName","Provider::SetCreationClassName","SetCreationClassName","SetCreationClassName method [Windows Management Instrumentation]","SetCreationClassName method [Windows Management Instrumentation]","Provider interface","_hmm_provider_setcreationclassname","provider/Provider::SetCreationClassName","wmi.provider_setcreationclassname"]
old-location: wmi\provider_setcreationclassname.htm
tech.root: wmi
ms.assetid: 0a02e767-95b7-42cb-ab82-66e2d28342fc
ms.date: 12/05/2018
ms.keywords: Provider interface [Windows Management Instrumentation],SetCreationClassName method, Provider.SetCreationClassName, Provider::SetCreationClassName, SetCreationClassName, SetCreationClassName method [Windows Management Instrumentation], SetCreationClassName method [Windows Management Instrumentation],Provider interface, _hmm_provider_setcreationclassname, provider/Provider::SetCreationClassName, wmi.provider_setcreationclassname
req.header: provider.h
req.include-header: FwCommon.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Provider::SetCreationClassName
 - provider/Provider::SetCreationClassName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - Provider.SetCreationClassName
---

# Provider::SetCreationClassName


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/provider/nl-provider-provider">Provider</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>SetCreationClassName</b> method sets the <b>CreationClassName</b> string property, if any, of the given instance to the name of this provider.

## -parameters

### -param pInstance

Pointer to the affected instance.

## -returns

Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if it was unsuccessful.

## -remarks

The <b>SetCreationClassName</b> method sets the value of the <b>CreateClassName</b> property to the name of the current class. Not all classes have a <b>CreationClassName</b> property.