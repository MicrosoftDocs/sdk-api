---
UID: NF:provider.Provider.Commit
title: Provider::Commit (provider.h)
description: The Commit method is used to send an instance to WMI. This method is a helper function and should not be overridden.
helpviewer_keywords: ["?Commit@Provider@@IAEJPAVCInstance@@_N@Z","?Commit@Provider@@IEAAJPEAVCInstance@@_N@Z","Commit","Commit method [Windows Management Instrumentation]","Commit method [Windows Management Instrumentation]","Provider interface","Provider interface [Windows Management Instrumentation]","Commit method","Provider.Commit","Provider::Commit","_hmm_provider_commit","provider/Provider::Commit","wmi.provider_commit"]
old-location: wmi\provider_commit.htm
tech.root: wmi
ms.assetid: 619adf78-26db-4a90-90ba-bdacb3e55975
ms.date: 12/05/2018
ms.keywords: ?Commit@Provider@@IAEJPAVCInstance@@_N@Z, ?Commit@Provider@@IEAAJPEAVCInstance@@_N@Z, Commit, Commit method [Windows Management Instrumentation], Commit method [Windows Management Instrumentation],Provider interface, Provider interface [Windows Management Instrumentation],Commit method, Provider.Commit, Provider::Commit, _hmm_provider_commit, provider/Provider::Commit, wmi.provider_commit
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
 - Provider::Commit
 - provider/Provider::Commit
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllCommit
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - Provider.Commit
 - ?Commit@Provider@@IAEJPAVCInstance@@_N@Z
 - ?Commit@Provider@@IEAAJPEAVCInstance@@_N@Z
---

# Provider::Commit


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/provider/nl-provider-provider">Provider</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>Commit</b> method is used to send an instance to WMI. This method is a helper function and should not be overridden.

## -parameters

### -param pInstance

Pointer to the instance to be stored by WMI.

### -param bCache

Indicates whether a cache is implemented. This value must be set to <b>FALSE</b> in the current version of the provider framework.

## -returns

Use the <b>SUCCEEDED</b> or <b>FAILED</b> macros on the returned HRESULT to determine if the method was successful.

## -remarks

If the client cancels the query, the <b>Commit</b> method returns an error. A provider writer can use this fact to terminate an enumeration.

Also, this method calls CInstance::Release on the <i>pInstance</i> pointer. Because of this, the framework provider must be careful not to call CInstance::Release again. This means that a <i>pInstance</i> smart pointer is incompatible with this method because the smart pointer calls CInstance::Release in its destructor.

This method should only be used when the framework provider does not call CInstance::Release on the <i>pInstance</i> pointer separately and if the <i>pInstance</i> pointer is not, and will never be, a smart pointer.