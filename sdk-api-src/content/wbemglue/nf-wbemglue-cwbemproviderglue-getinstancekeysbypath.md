---
UID: NF:wbemglue.CWbemProviderGlue.GetInstanceKeysByPath
title: CWbemProviderGlue::GetInstanceKeysByPath (wbemglue.h)
description: The GetInstanceKeysByPath method retrieves the instance identified by a particular object path, with only the key properties populated.
helpviewer_keywords: ["CWbemProviderGlue interface [Windows Management Instrumentation]","GetInstanceKeysByPath method","CWbemProviderGlue.GetInstanceKeysByPath","CWbemProviderGlue::GetInstanceKeysByPath","GetInstanceKeysByPath","GetInstanceKeysByPath method [Windows Management Instrumentation]","GetInstanceKeysByPath method [Windows Management Instrumentation]","CWbemProviderGlue interface","_hmm_cwbemproviderglue_getinstancekeysbypath","wbemglue/CWbemProviderGlue::GetInstanceKeysByPath","wmi.cwbemproviderglue_getinstancekeysbypath"]
old-location: wmi\cwbemproviderglue_getinstancekeysbypath.htm
tech.root: wmi
ms.assetid: 8ae95850-59e9-4382-b88d-c51eb3077176
ms.date: 12/05/2018
ms.keywords: CWbemProviderGlue interface [Windows Management Instrumentation],GetInstanceKeysByPath method, CWbemProviderGlue.GetInstanceKeysByPath, CWbemProviderGlue::GetInstanceKeysByPath, GetInstanceKeysByPath, GetInstanceKeysByPath method [Windows Management Instrumentation], GetInstanceKeysByPath method [Windows Management Instrumentation],CWbemProviderGlue interface, _hmm_cwbemproviderglue_getinstancekeysbypath, wbemglue/CWbemProviderGlue::GetInstanceKeysByPath, wmi.cwbemproviderglue_getinstancekeysbypath
req.header: wbemglue.h
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
 - CWbemProviderGlue::GetInstanceKeysByPath
 - wbemglue/CWbemProviderGlue::GetInstanceKeysByPath
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
 - CWbemProviderGlue.GetInstanceKeysByPath
---

# CWbemProviderGlue::GetInstanceKeysByPath


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/wbemglue/nl-wbemglue-cwbemproviderglue">CWbemProviderGlue</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetInstanceKeysByPath</b> method retrieves the instance identified by a particular object path, with only the key properties populated.

## -parameters

### -param pszInstancePath

An object path to the instance to be returned.

### -param ppInstance

A pointer to a pointer to a new <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> instance whose keys are those specified in the <i>pszInstancePath</i>. The framework provider the performs the request must release this pointer.

### -param pMethodContext

A pointer to the current context. A context must be provided to prevent deadlocks. Either use the context passed into the provider by <a href="/windows/desktop/api/provider/nf-provider-provider-enumerateinstances">Provider::EnumerateInstances</a> or <a href="/windows/desktop/api/provider/nf-provider-provider-execquery">Provider::ExecQuery</a>, or else obtain it from the instance using <a href="/windows/desktop/api/instance/nf-instance-cinstance-getmethodcontext">CInstance::GetMethodContext</a>. This parameter must not be <b>NULL</b>.

## -returns

Returns <b>WBEM_S_NO_ERROR</b> if the operation was successful, <b>WBEM_E_OUT_OF_MEMORY</b> if the operation failed due to lack of memory, or any other <b>HRESULT</b> error code.

## -remarks

This method makes use of partial-instance update operations to request only the key properties of the specified object. It is the most efficient way to verify the existence of a specific object. Be aware that not all providers support partial-instance operations. In that case, the entire instance will be populated. For more information, see <a href="/windows/desktop/WmiSdk/supporting-partial-instance-operations">Supporting Partial-Instance Operations</a>.

In the current version of the provider framework, <i>pszInstancePath</i> must resolve to be an instance path on the same computer.

## -see-also

<a href="/windows/desktop/api/wbemglue/nl-wbemglue-cwbemproviderglue">CWbemProviderGlue</a>



<a href="/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getinstancebypath(lpcwstr_cinstance_methodcontext)">GetInstanceByPath</a>



<a href="/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getinstancepropertiesbypath">GetInstancePropertiesByPath</a>