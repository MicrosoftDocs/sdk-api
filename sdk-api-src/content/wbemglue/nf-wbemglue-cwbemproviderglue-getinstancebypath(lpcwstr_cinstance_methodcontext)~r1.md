---
UID: NF:wbemglue.CWbemProviderGlue.GetInstanceByPath(LPCWSTR,CInstance,MethodContext)~r1
title: CWbemProviderGlue::GetInstanceByPath (wbemglue.h)
description: The CWbemProviderGlue::GetInstanceByPath (wbemglue.h) method retrieves the instance identified by a particular object path by calling the provider GetObject method.
helpviewer_keywords: ["?GetInstanceByPath@CWbemProviderGlue@@SAJPEBGPEAPEAVCInstance@@PEAVMethodContext@@@Z","?GetInstanceByPath@CWbemProviderGlue@@SGJPBGPAPAVCInstance@@PAVMethodContext@@@Z","CWbemProviderGlue interface [Windows Management Instrumentation]","GetInstanceByPath method","CWbemProviderGlue.GetInstanceByPath","CWbemProviderGlue::GetInstanceByPath","GetInstanceByPath","GetInstanceByPath method [Windows Management Instrumentation]","GetInstanceByPath method [Windows Management Instrumentation]","CWbemProviderGlue interface","_hmm_cwbemproviderglue_getinstancebypath","wbemglue/CWbemProviderGlue::GetInstanceByPath","wmi.cwbemproviderglue_getinstancebypath"]
old-location: wmi\cwbemproviderglue_getinstancebypath.htm
tech.root: wmi
ms.assetid: 788b5f5f-b300-4c86-afbd-416b938f21c1
ms.date: 08/15/2022
ms.keywords: ?GetInstanceByPath@CWbemProviderGlue@@SAJPEBGPEAPEAVCInstance@@PEAVMethodContext@@@Z, ?GetInstanceByPath@CWbemProviderGlue@@SGJPBGPAPAVCInstance@@PAVMethodContext@@@Z, CWbemProviderGlue interface [Windows Management Instrumentation],GetInstanceByPath method, CWbemProviderGlue.GetInstanceByPath, CWbemProviderGlue::GetInstanceByPath, GetInstanceByPath, GetInstanceByPath method [Windows Management Instrumentation], GetInstanceByPath method [Windows Management Instrumentation],CWbemProviderGlue interface, _hmm_cwbemproviderglue_getinstancebypath, wbemglue/CWbemProviderGlue::GetInstanceByPath, wmi.cwbemproviderglue_getinstancebypath
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
 - CWbemProviderGlue::GetInstanceByPath
 - wbemglue/CWbemProviderGlue::GetInstanceByPath
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
 - CWbemProviderGlue.GetInstanceByPath
 - ?GetInstanceByPath@CWbemProviderGlue@@SAJPEBGPEAPEAVCInstance@@PEAVMethodContext@@@Z
 - ?GetInstanceByPath@CWbemProviderGlue@@SGJPBGPAPAVCInstance@@PAVMethodContext@@@Z
---

# CWbemProviderGlue::GetInstanceByPath


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/wbemglue/nl-wbemglue-cwbemproviderglue">CWbemProviderGlue</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetInstanceByPath</b> method 
    retrieves the instance identified by a particular object path by calling the provider 
    <a href="/windows/desktop/api/provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)">GetObject</a> method.

## -parameters

### -param pszObjectPath

An object path to the instance to be returned.

### -param ppInstance

A pointer to a pointer to a <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> instance used to 
      store the new instance. The framework provider that performs the request must release this pointer.

### -param pMethodContext

A pointer to the current context. A context must be provided to prevent deadlocks. Either use the context 
      passed into the provider by 
      <a href="/windows/desktop/api/provider/nf-provider-provider-enumerateinstances">Provider::EnumerateInstances</a> or 
      <a href="/windows/desktop/api/provider/nf-provider-provider-execquery">Provider::ExecQuery</a>, or else obtain it from the 
      instance using <a href="/windows/desktop/api/instance/nf-instance-cinstance-getmethodcontext">CInstance::GetMethodContext</a>. 
      This parameter must not be <b>NULL</b>.

## -returns

Returns <b>WBEM_S_NO_ERROR</b> if the operation was successful, 
       <b>WBEM_E_OUT_OF_MEMORY</b> if the operation failed due to lack of memory, or any other 
       <b>HRESULT</b> error code.

## -remarks

The <b>GetInstanceByPath</b> method 
    allows framework providers to access data from another provider without requiring a WMI API call. Framework 
    providers pass the object path of an instance to 
    <b>GetInstanceByPath</b>, which returns the 
    instance.

In the current version of the provider framework, <i>pszInstancePath</i> must resolve to be 
    an instance path on the same computer.

Although <i>pMethodContext</i> has a default value of <b>NULL</b>, a 
    context must be provided to prevent deadlocks. Either use the context passed into the provider by 
    <a href="/windows/desktop/api/provider/nf-provider-provider-enumerateinstances">Provider::EnumerateInstances</a> or 
    <a href="/windows/desktop/api/provider/nf-provider-provider-execquery">Provider::ExecQuery</a>, or else obtain it from the 
    instance using 
    <a href="/windows/desktop/api/instance/nf-instance-cinstance-getmethodcontext">CInstance::GetMethodContext</a>.