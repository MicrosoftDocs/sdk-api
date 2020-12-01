---
UID: NF:provider.Provider.Provider
title: Provider::Provider (provider.h)
description: The Provider method creates an instance of a provider. This method is part of the WMI Provider Framework.
helpviewer_keywords: ["??0Provider@@QAE@PBG0@Z","??0Provider@@QEAA@PEBG0@Z","Provider","Provider interface [Windows Management Instrumentation]","Provider method","Provider method [Windows Management Instrumentation]","Provider method [Windows Management Instrumentation]","Provider interface","Provider.Provider","Provider::Provider","provider/Provider::Provider","wmi.provider_provider"]
old-location: wmi\provider_provider.htm
tech.root: wmi
ms.assetid: 1859c921-a0dc-4fd4-9c0b-680a24eab936
ms.date: 12/05/2018
ms.keywords: ??0Provider@@QAE@PBG0@Z, ??0Provider@@QEAA@PEBG0@Z, Provider, Provider interface [Windows Management Instrumentation],Provider method, Provider method [Windows Management Instrumentation], Provider method [Windows Management Instrumentation],Provider interface, Provider.Provider, Provider::Provider, provider/Provider::Provider, wmi.provider_provider
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
 - Provider::Provider
 - provider/Provider::Provider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - Provider.Provider
 - ??0Provider@@QAE@PBG0@Z
 - ??0Provider@@QEAA@PEBG0@Z
---

# Provider::Provider


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/provider/nl-provider-provider">Provider</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>Provider</b> method creates an instance of a provider. This method is part of the WMI Provider Framework.

## -parameters

### -param a_pszName

Name of the provider to be instantiated.

### -param a_pszNameSpace

<b>NULL</b>

## -remarks

The destructor for the <a href="/windows/desktop/api/provider/nl-provider-provider">Provider</a> class is <b>Provider::~Provider</b>.