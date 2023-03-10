---
UID: NF:wbemglue.CWbemProviderGlue.IsDerivedFrom(LPCWSTR,LPCWSTR,MethodContext,LPCWSTR)~r1
title: CWbemProviderGlue::IsDerivedFrom (wbemglue.h)
description: The CWbemProviderGlue::IsDerivedFrom (wbemglue.h) method determines whether one class is derived from another.
helpviewer_keywords: ["CWbemProviderGlue interface [Windows Management Instrumentation]","IsDerivedFrom method","CWbemProviderGlue.IsDerivedFrom","CWbemProviderGlue::IsDerivedFrom","IsDerivedFrom","IsDerivedFrom method [Windows Management Instrumentation]","IsDerivedFrom method [Windows Management Instrumentation]","CWbemProviderGlue interface","_hmm_cwbemproviderglue_isderivedfrom","wbemglue/CWbemProviderGlue::IsDerivedFrom","wmi.cwbemproviderglue_isderivedfrom"]
old-location: wmi\cwbemproviderglue_isderivedfrom.htm
tech.root: wmi
ms.assetid: e8245511-d192-4489-b907-45de1d354c49
ms.date: 08/15/2022
ms.keywords: CWbemProviderGlue interface [Windows Management Instrumentation],IsDerivedFrom method, CWbemProviderGlue.IsDerivedFrom, CWbemProviderGlue::IsDerivedFrom, IsDerivedFrom, IsDerivedFrom method [Windows Management Instrumentation], IsDerivedFrom method [Windows Management Instrumentation],CWbemProviderGlue interface, _hmm_cwbemproviderglue_isderivedfrom, wbemglue/CWbemProviderGlue::IsDerivedFrom, wmi.cwbemproviderglue_isderivedfrom
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
 - CWbemProviderGlue::IsDerivedFrom
 - wbemglue/CWbemProviderGlue::IsDerivedFrom
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
 - CWbemProviderGlue.IsDerivedFrom
---

# CWbemProviderGlue::IsDerivedFrom


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/wbemglue/nl-wbemglue-cwbemproviderglue">CWbemProviderGlue</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>IsDerivedFrom</b> method determines whether one class is derived from another.

## -parameters

### -param pszBaseClassName

Name of base class.

### -param pszDerivedClassName

Name of class to be tested.

### -param pMethodContext

Pointer to the current context. A context must be provided to prevent deadlocks. Either use the context passed into the provider by <a href="/windows/desktop/api/provider/nf-provider-provider-enumerateinstances">Provider::EnumerateInstances</a> or <a href="/windows/desktop/api/provider/nf-provider-provider-execquery">Provider::ExecQuery</a>, or else obtain it from the instance using <a href="/windows/desktop/api/instance/nf-instance-cinstance-getmethodcontext">CInstance::GetMethodContext</a>. This parameter must not be <b>NULL</b>.

### -param pszNamespace

Namespace that contains <i>pszBaseClassName</i> and <i>pszDerivedClassname</i>. If <b>NULL</b>, the default namespace, root\cimv2, is used.

## -returns

The method returns <b>TRUE</b> if the class pointed to by <i>pszDerivedClassName</i> is a subclass of the class pointed to by <i>pszBaseClassName</i> and <b>FALSE</b> if <i>pszDerivedClassName</i> does not derive from <i>pszBaseClassName</i>. If asked if a class is derived from itself, this method returns <b>FALSE</b>.