---
UID: NF:provider.Provider.MakeLocalPath
title: Provider::MakeLocalPath (provider.h)
description: The MakeLocalPath method builds a full instance path from a relative path.
helpviewer_keywords: ["MakeLocalPath","MakeLocalPath method [Windows Management Instrumentation]","MakeLocalPath method [Windows Management Instrumentation]","Provider interface","Provider interface [Windows Management Instrumentation]","MakeLocalPath method","Provider.MakeLocalPath","Provider::MakeLocalPath","_hmm_provider_makelocalpath","provider/Provider::MakeLocalPath","wmi.provider_makelocalpath"]
old-location: wmi\provider_makelocalpath.htm
tech.root: wmi
ms.assetid: 8a2476c0-73c0-4a95-8973-e6da451116af
ms.date: 12/05/2018
ms.keywords: MakeLocalPath, MakeLocalPath method [Windows Management Instrumentation], MakeLocalPath method [Windows Management Instrumentation],Provider interface, Provider interface [Windows Management Instrumentation],MakeLocalPath method, Provider.MakeLocalPath, Provider::MakeLocalPath, _hmm_provider_makelocalpath, provider/Provider::MakeLocalPath, wmi.provider_makelocalpath
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
 - Provider::MakeLocalPath
 - provider/Provider::MakeLocalPath
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
 - Provider.MakeLocalPath
---

# Provider::MakeLocalPath


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/provider/nl-provider-provider">Provider</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>MakeLocalPath</b> method builds a full instance path from a relative path.

## -parameters

### -param strRelPath [ref]

Relative path used to build the full path.

## -returns

Returns the full path in <a href="/windows/desktop/WmiSdk/chstring">CHString</a> format.

## -remarks

Consider using <a href="/windows/desktop/api/provider/nf-provider-provider-getlocalinstancepath">Provider::GetLocalInstancePath</a> before using this method.