---
UID: NF:provider.Provider.GetLocalInstancePath
title: Provider::GetLocalInstancePath method
author: windows-driver-content
description: The GetLocalInstancePath method attempts to build a full object path to a specified instance. This method is a helper function and should not be overridden.
old-location: wmi\provider_getlocalinstancepath.htm
old-project: WmiSdk
ms.assetid: c419205f-d07d-4887-8e36-ccde37c2351f
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: GetLocalInstancePath method [Windows Management Instrumentation], GetLocalInstancePath method [Windows Management Instrumentation], Provider interface, GetLocalInstancePath,Provider.GetLocalInstancePath, Provider, Provider interface [Windows Management Instrumentation], GetLocalInstancePath method, Provider::GetLocalInstancePath, _hmm_provider_getlocalinstancepath, provider/Provider::GetLocalInstancePath, wmi.provider_getlocalinstancepath
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
-	Provider.GetLocalInstancePath
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# Provider::GetLocalInstancePath method


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/library/windows/hardware/hh406455">Provider</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetLocalInstancePath</b> method attempts to build a full object path to a specified instance. This method is a helper function and should not be overridden.


## -parameters




### -param pInstance [in]

Pointer to the instance for which the path should be built.


### -param strPath [out, ref]

Full object path, complete from the computer name to the key value.


## -returns



Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if the operation was unsuccessful.



