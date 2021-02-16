---
UID: NF:provider.Provider.GetLocalInstancePath
title: Provider::GetLocalInstancePath (provider.h)
description: The GetLocalInstancePath method attempts to build a full object path to a specified instance. This method is a helper function and should not be overridden.
helpviewer_keywords: ["GetLocalInstancePath","GetLocalInstancePath method [Windows Management Instrumentation]","GetLocalInstancePath method [Windows Management Instrumentation]","Provider interface","Provider interface [Windows Management Instrumentation]","GetLocalInstancePath method","Provider.GetLocalInstancePath","Provider::GetLocalInstancePath","_hmm_provider_getlocalinstancepath","provider/Provider::GetLocalInstancePath","wmi.provider_getlocalinstancepath"]
old-location: wmi\provider_getlocalinstancepath.htm
tech.root: wmi
ms.assetid: c419205f-d07d-4887-8e36-ccde37c2351f
ms.date: 12/05/2018
ms.keywords: GetLocalInstancePath, GetLocalInstancePath method [Windows Management Instrumentation], GetLocalInstancePath method [Windows Management Instrumentation],Provider interface, Provider interface [Windows Management Instrumentation],GetLocalInstancePath method, Provider.GetLocalInstancePath, Provider::GetLocalInstancePath, _hmm_provider_getlocalinstancepath, provider/Provider::GetLocalInstancePath, wmi.provider_getlocalinstancepath
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
 - Provider::GetLocalInstancePath
 - provider/Provider::GetLocalInstancePath
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
 - Provider.GetLocalInstancePath
---

# Provider::GetLocalInstancePath


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/provider/nl-provider-provider">Provider</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetLocalInstancePath</b> method attempts to build a full object path to a specified instance. This method is a helper function and should not be overridden.

## -parameters

### -param pInstance [in]

Pointer to the instance for which the path should be built.

### -param strPath [out, ref]

Full object path, complete from the computer name to the key value.

## -returns

Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if the operation was unsuccessful.