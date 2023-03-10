---
UID: NF:wbemglue.CWbemProviderGlue.GetEmptyInstance(MethodContext,LPCWSTR,CInstance,LPCWSTR)
title: CWbemProviderGlue::GetEmptyInstance(MethodContext,LPCWSTR,CInstance,LPCWSTR) (wbemglue.h)
description: The GetEmptyInstance method retrieves a single unpopulated instance of the specified class. (overload 2/2)
helpviewer_keywords: ["?GetEmptyInstance@CWbemProviderGlue@@SGJPAVMethodContext@@PBGPAPAVCInstance@@1@Z","CWbemProviderGlue interface [Windows Management Instrumentation]","GetEmptyInstance method","CWbemProviderGlue.GetEmptyInstance","CWbemProviderGlue.GetEmptyInstance(MethodContext","LPCWSTR","CInstance","LPCWSTR)","CWbemProviderGlue::GetEmptyInstance","CWbemProviderGlue::GetEmptyInstance(MethodContext*","LPCWSTR","CInstance**","LPCWSTR)","CWbemProviderGlue::GetEmptyInstance(MethodContext","LPCWSTR","CInstance","LPCWSTR)","GetEmptyInstance","GetEmptyInstance method [Windows Management Instrumentation]","GetEmptyInstance method [Windows Management Instrumentation]","CWbemProviderGlue interface","wbemglue/CWbemProviderGlue::GetEmptyInstance","wmi.cwbemproviderglue_getemptyinstance_methodcontext_lpcwstr_cinstance__lpcwstr_"]
old-location: wmi\cwbemproviderglue_getemptyinstance_methodcontext_lpcwstr_cinstance__lpcwstr_.htm
tech.root: wmi
ms.assetid: 001135bf-5ef5-41ca-9b14-257ea672a3b7
ms.date: 12/05/2018
ms.keywords: ?GetEmptyInstance@CWbemProviderGlue@@SGJPAVMethodContext@@PBGPAPAVCInstance@@1@Z, CWbemProviderGlue interface [Windows Management Instrumentation],GetEmptyInstance method, CWbemProviderGlue.GetEmptyInstance, CWbemProviderGlue.GetEmptyInstance(MethodContext,LPCWSTR,CInstance,LPCWSTR), CWbemProviderGlue::GetEmptyInstance, CWbemProviderGlue::GetEmptyInstance(MethodContext*,LPCWSTR,CInstance**,LPCWSTR), CWbemProviderGlue::GetEmptyInstance(MethodContext,LPCWSTR,CInstance,LPCWSTR), GetEmptyInstance, GetEmptyInstance method [Windows Management Instrumentation], GetEmptyInstance method [Windows Management Instrumentation],CWbemProviderGlue interface, wbemglue/CWbemProviderGlue::GetEmptyInstance, wmi.cwbemproviderglue_getemptyinstance_methodcontext_lpcwstr_cinstance__lpcwstr_
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
 - CWbemProviderGlue::GetEmptyInstance
 - wbemglue/CWbemProviderGlue::GetEmptyInstance
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
 - CWbemProviderGlue.GetEmptyInstance
 - ?GetEmptyInstance@CWbemProviderGlue@@SGJPAVMethodContext@@PBGPAPAVCInstance@@1@Z
---

# CWbemProviderGlue::GetEmptyInstance(MethodContext,LPCWSTR,CInstance,LPCWSTR)


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/wbemglue/nl-wbemglue-cwbemproviderglue">CWbemProviderGlue</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetEmptyInstance</b> method retrieves a single unpopulated instance of the specified class.

## -parameters

### -param pMethodContext

Pointer to the current context.

### -param pszClassName

Name of the class whose instance is to be returned.

### -param ppInstance

Pointer to an instance of the <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class used to store the new instance. This pointer must be released by the framework provider calling <b>GetEmptyInstance</b>.

### -param pszNamespace

Namespace of the class name specified by <i>pszClassName</i>. This parameter can be <b>NULL</b> to indicate the default namespace, which is root\cimv2.

## -returns

Returns <b>WBEM_S_NO_ERROR</b> if the operation was successful, <b>WBEM_E_OUT_OF_MEMORY</b> if the operation failed due to lack of memory, or any other <b>HRESULT</b> error code.

## -remarks

The framework provider pass the name of the provider to <b>GetEmptyInstance</b>, which returns an empty instance. A common use of this method is to populate an embedded object property. This method is used in conjunction with <a href="/windows/desktop/api/instance/nf-instance-cinstance-setembeddedobject">CInstance::SetEmbeddedObject</a>.

The second function prototype is not recommended. It is provided only to support existing code.
