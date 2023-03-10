---
UID: NF:provider.Provider.GetNamespace
title: Provider::GetNamespace (provider.h)
description: The GetNamespace method returns a constant reference to the namespace name in CHString format. The name returned is the second parameter originally given to the provider constructor.
helpviewer_keywords: ["GetNamespace","GetNamespace method [Windows Management Instrumentation]","GetNamespace method [Windows Management Instrumentation]","Provider interface","Provider interface [Windows Management Instrumentation]","GetNamespace method","Provider.GetNamespace","Provider::GetNamespace","_hmm_provider_getnamespace","provider/Provider::GetNamespace","wmi.provider_getnamespace"]
old-location: wmi\provider_getnamespace.htm
tech.root: wmi
ms.assetid: aa400731-3127-4ea7-a4ac-f31b6af8db98
ms.date: 12/05/2018
ms.keywords: GetNamespace, GetNamespace method [Windows Management Instrumentation], GetNamespace method [Windows Management Instrumentation],Provider interface, Provider interface [Windows Management Instrumentation],GetNamespace method, Provider.GetNamespace, Provider::GetNamespace, _hmm_provider_getnamespace, provider/Provider::GetNamespace, wmi.provider_getnamespace
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
 - Provider::GetNamespace
 - provider/Provider::GetNamespace
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
 - Provider.GetNamespace
---

# Provider::GetNamespace


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/provider/nl-provider-provider">Provider</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetNamespace</b> method returns a constant reference to the namespace name in <a href="/windows/desktop/WmiSdk/chstring">CHString</a> format. The name returned is the second parameter originally given to the provider constructor.



## -returns

Returns a constant reference to the namespace.
