---
UID: NF:provider.Provider.SetCreationClassName
title: Provider::SetCreationClassName method
author: windows-driver-content
description: The SetCreationClassName method sets the CreationClassName string property, if any, of the given instance to the name of this provider.
old-location: wmi\provider_setcreationclassname.htm
old-project: WmiSdk
ms.assetid: 0a02e767-95b7-42cb-ab82-66e2d28342fc
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: Provider, Provider interface [Windows Management Instrumentation], SetCreationClassName method, Provider::SetCreationClassName, SetCreationClassName method [Windows Management Instrumentation], SetCreationClassName method [Windows Management Instrumentation], Provider interface, SetCreationClassName,Provider.SetCreationClassName, _hmm_provider_setcreationclassname, provider/Provider::SetCreationClassName, wmi.provider_setcreationclassname
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FrameDynOS.dll
-	FrameDyn.dll
api_name:
-	Provider.SetCreationClassName
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# Provider::SetCreationClassName method


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/library/windows/hardware/hh406455">Provider</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>SetCreationClassName</b> method sets the <b>CreationClassName</b> string property, if any, of the given instance to the name of this provider.


## -parameters




### -param pInstance

Pointer to the affected instance.


## -returns



Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if it was unsuccessful.




## -remarks



The <b>SetCreationClassName</b> method sets the value of the <b>CreateClassName</b> property to the name of the current class. Not all classes have a <b>CreationClassName</b> property.



