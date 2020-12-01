---
UID: NF:wbemglue.CWbemProviderGlue.GetInstancePropertiesByPath
title: CWbemProviderGlue::GetInstancePropertiesByPath (wbemglue.h)
description: Retrieves the instance identified by a particular object path, with only the specified properties populated. The properties to be populated are named in a CHString array.
helpviewer_keywords: ["CWbemProviderGlue interface [Windows Management Instrumentation]","GetInstancePropertiesByPath method","CWbemProviderGlue.GetInstancePropertiesByPath","CWbemProviderGlue::GetInstancePropertiesByPath","GetInstancePropertiesByPath","GetInstancePropertiesByPath method [Windows Management Instrumentation]","GetInstancePropertiesByPath method [Windows Management Instrumentation]","CWbemProviderGlue interface","_hmm_cwbemproviderglue_getinstancepropertiesbypath","wbemglue/CWbemProviderGlue::GetInstancePropertiesByPath","wmi.cwbemproviderglue_getinstancepropertiesbypath"]
old-location: wmi\cwbemproviderglue_getinstancepropertiesbypath.htm
tech.root: wmi
ms.assetid: d9232dc0-6df9-440d-bf7a-bf524acbe505
ms.date: 12/05/2018
ms.keywords: CWbemProviderGlue interface [Windows Management Instrumentation],GetInstancePropertiesByPath method, CWbemProviderGlue.GetInstancePropertiesByPath, CWbemProviderGlue::GetInstancePropertiesByPath, GetInstancePropertiesByPath, GetInstancePropertiesByPath method [Windows Management Instrumentation], GetInstancePropertiesByPath method [Windows Management Instrumentation],CWbemProviderGlue interface, _hmm_cwbemproviderglue_getinstancepropertiesbypath, wbemglue/CWbemProviderGlue::GetInstancePropertiesByPath, wmi.cwbemproviderglue_getinstancepropertiesbypath
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
 - CWbemProviderGlue::GetInstancePropertiesByPath
 - wbemglue/CWbemProviderGlue::GetInstancePropertiesByPath
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
 - CWbemProviderGlue.GetInstancePropertiesByPath
---

# CWbemProviderGlue::GetInstancePropertiesByPath


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/wbemglue/nl-wbemglue-cwbemproviderglue">CWbemProviderGlue</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetInstancePropertiesByPath</b> method retrieves the instance identified by a particular object path, with only the specified properties populated. The properties to be populated are named in a <a href="/windows/desktop/WmiSdk/chstring">CHString</a> array.

## -parameters

### -param pszInstancePath

The object path to the instance to be returned. This parameter must point to a full path.

### -param ppInstance

A pointer to a pointer to a new <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> instance whose keys are those specified by <i>pszInstancePath</i>. The framework provider that performs the request is must release this pointer.

### -param pMethodContext

A pointer to the current context. A context must be provided to prevent deadlocks. Either use the context passed into the provider by <a href="/windows/desktop/api/provider/nf-provider-provider-enumerateinstances">Provider::EnumerateInstances</a> or <a href="/windows/desktop/api/provider/nf-provider-provider-execquery">Provider::ExecQuery</a>, or else obtain it from the instance using <a href="/windows/desktop/api/instance/nf-instance-cinstance-getmethodcontext">CInstance::GetMethodContext</a>. This parameter must not be <b>NULL</b>.

### -param csaProperties [ref]

An array that contains the names of the properties to be copied into the new instance.

## -returns

Returns <b>WBEM_S_NO_ERROR</b> if the operation was successful, <b>WBEM_E_OUT_OF_MEMORY</b> if the operation failed due to lack of memory, or any other <b>HRESULT</b> error code.

## -remarks

This method makes use of partial-instance update operations to request only the specified properties of the specified object. This is the most efficient way to retrieve a specific instance when more properties than just the keys are required. Be aware that not all providers support partial-instance operations. In that case, the entire instance (including the keys) are populated. For more information, see <a href="/windows/desktop/WmiSdk/supporting-partial-instance-operations">Supporting Partial-Instance Operations</a>.

In the current version of the provider framework, <i>pszInstancePath</i> must resolve to be an instance path on the same computer.

## -see-also

<a href="/windows/desktop/api/wbemglue/nl-wbemglue-cwbemproviderglue">CWbemProviderGlue</a>



<a href="/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getinstancebypath(lpcwstr_cinstance_methodcontext)">GetInstanceByPath</a>



<a href="/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getinstancekeysbypath">GetInstanceKeysByPath</a>