---
UID: NF:provider.Provider.GetProviderName
title: Provider::GetProviderName
author: windows-sdk-content
description: The GetProviderName method retrieves the name of the class used in the constructor of the provider.
old-location: wmi\provider_getprovidername.htm
old-project: WmiSdk
ms.assetid: 9ea7558d-11bd-4f19-b4d3-a711eca632a8
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: GetProviderName, GetProviderName method [Windows Management Instrumentation], GetProviderName method [Windows Management Instrumentation],Provider interface, Provider interface [Windows Management Instrumentation],GetProviderName method, Provider.GetProviderName, Provider::GetProviderName, _hmm_provider_getprovidername, provider/Provider::GetProviderName, wmi.provider_getprovidername
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: provider.h
req.include-header: FwCommon.h
req.redist: 
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
tech.root: 
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - Provider.GetProviderName
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: ADAM
---

# Provider::GetProviderName


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/d8a7c433-7e6a-45cc-914f-a15a3688c7aa">Provider</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetProviderName</b> method retrieves the name of the class used in the constructor of the provider.


## -parameters






## -returns



If successful, the method returns the name of the class used in the constructor of the provider as a <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> reference. The name returned is the first parameter originally given to the Provider::Provider constructor.



