---
UID: NF:provider.Provider.Provider
title: Provider::Provider method
author: windows-driver-content
description: The Provider method creates an instance of a provider. This method is part of the WMI Provider Framework.
old-location: wmi\provider_provider.htm
old-project: WmiSdk
ms.assetid: 1859c921-a0dc-4fd4-9c0b-680a24eab936
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: "??0Provider@@QAE@PBG0@Z, ??0Provider@@QEAA@PEBG0@Z, Provider, Provider interface [Windows Management Instrumentation], Provider method, Provider method [Windows Management Instrumentation], Provider method [Windows Management Instrumentation], Provider interface, Provider,Provider.Provider, Provider::Provider, provider/Provider::Provider, wmi.provider_provider"
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
-	Provider.Provider
-	??0Provider@@QAE@PBG0@Z
-	??0Provider@@QEAA@PEBG0@Z
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# Provider::Provider method


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/library/windows/hardware/hh406455">Provider</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>Provider</b> method creates an instance of a provider. This method is part of the WMI Provider Framework.


## -parameters




### -param a_pszName

Name of the provider to be instantiated.


### -param a_pszNameSpace






#### - a_pszNameSpace = NULL

<b>NULL</b>

## -returns



This method does not return a value.




## -remarks



The destructor for the <a href="https://msdn.microsoft.com/library/windows/hardware/hh406455">Provider</a> class is <b>Provider::~Provider</b>.



