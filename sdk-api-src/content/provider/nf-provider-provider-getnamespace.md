---
UID: NF:provider.Provider.GetNamespace
title: Provider::GetNamespace method
author: windows-driver-content
description: The GetNamespace method returns a constant reference to the namespace name in CHString format. The name returned is the second parameter originally given to the provider constructor.
old-location: wmi\provider_getnamespace.htm
old-project: WmiSdk
ms.assetid: aa400731-3127-4ea7-a4ac-f31b6af8db98
ms.author: windowsdriverdev
ms.date: 3/16/2018
ms.keywords: GetNamespace method [Windows Management Instrumentation], GetNamespace method [Windows Management Instrumentation], Provider interface, GetNamespace,Provider.GetNamespace, Provider, Provider interface [Windows Management Instrumentation], GetNamespace method, Provider::GetNamespace, _hmm_provider_getnamespace, provider/Provider::GetNamespace, wmi.provider_getnamespace
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
-	Provider.GetNamespace
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# Provider::GetNamespace method


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/library/windows/hardware/hh406455">Provider</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetNamespace</b> method returns a constant reference to the namespace name in <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> format. The name returned is the second parameter originally given to the provider constructor.


## -parameters






## -returns



Returns a constant reference to the namespace.



