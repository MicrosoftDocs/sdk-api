---
UID: NF:provider.Provider.GetProviderName
title: Provider::GetProviderName (provider.h)
description: The GetProviderName method retrieves the name of the class used in the constructor of the provider.
helpviewer_keywords: ["GetProviderName","GetProviderName method [Windows Management Instrumentation]","GetProviderName method [Windows Management Instrumentation]","Provider interface","Provider interface [Windows Management Instrumentation]","GetProviderName method","Provider.GetProviderName","Provider::GetProviderName","_hmm_provider_getprovidername","provider/Provider::GetProviderName","wmi.provider_getprovidername"]
old-location: wmi\provider_getprovidername.htm
tech.root: wmi
ms.assetid: 9ea7558d-11bd-4f19-b4d3-a711eca632a8
ms.date: 12/05/2018
ms.keywords: GetProviderName, GetProviderName method [Windows Management Instrumentation], GetProviderName method [Windows Management Instrumentation],Provider interface, Provider interface [Windows Management Instrumentation],GetProviderName method, Provider.GetProviderName, Provider::GetProviderName, _hmm_provider_getprovidername, provider/Provider::GetProviderName, wmi.provider_getprovidername
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
 - Provider::GetProviderName
 - provider/Provider::GetProviderName
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
 - Provider.GetProviderName
---

# Provider::GetProviderName


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/provider/nl-provider-provider">Provider</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetProviderName</b> method retrieves the name of the class used in the constructor of the provider.



## -returns

If successful, the method returns the name of the class used in the constructor of the provider as a <a href="/windows/desktop/WmiSdk/chstring">CHString</a> reference. The name returned is the first parameter originally given to the Provider::Provider constructor.
