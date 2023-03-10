---
UID: NF:wbemglue.CWbemProviderGlue.GetAllInstances
title: CWbemProviderGlue::GetAllInstances (wbemglue.h)
description: The GetAllInstances method retrieves a list of instances returned by a specific class.
helpviewer_keywords: ["?GetAllInstances@CWbemProviderGlue@@SGJPBGPAV?$TRefPointerCollection@VCInstance@@@@0PAVMethodContext@@@Z","CWbemProviderGlue interface [Windows Management Instrumentation]","GetAllInstances method","CWbemProviderGlue.GetAllInstances","CWbemProviderGlue::GetAllInstances","GetAllInstances","GetAllInstances method [Windows Management Instrumentation]","GetAllInstances method [Windows Management Instrumentation]","CWbemProviderGlue interface","_hmm_cwbemproviderglue_getallinstances","wbemglue/CWbemProviderGlue::GetAllInstances","wmi.cwbemproviderglue_getallinstances"]
old-location: wmi\cwbemproviderglue_getallinstances.htm
tech.root: wmi
ms.assetid: 510d0711-ee82-4270-a7e3-f6bb214716a0
ms.date: 12/05/2018
ms.keywords: ?GetAllInstances@CWbemProviderGlue@@SGJPBGPAV?$TRefPointerCollection@VCInstance@@@@0PAVMethodContext@@@Z, CWbemProviderGlue interface [Windows Management Instrumentation],GetAllInstances method, CWbemProviderGlue.GetAllInstances, CWbemProviderGlue::GetAllInstances, GetAllInstances, GetAllInstances method [Windows Management Instrumentation], GetAllInstances method [Windows Management Instrumentation],CWbemProviderGlue interface, _hmm_cwbemproviderglue_getallinstances, wbemglue/CWbemProviderGlue::GetAllInstances, wmi.cwbemproviderglue_getallinstances
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
 - CWbemProviderGlue::GetAllInstances
 - wbemglue/CWbemProviderGlue::GetAllInstances
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
 - CWbemProviderGlue.GetAllInstances
 - ?GetAllInstances@CWbemProviderGlue@@SGJPBGPAV?$TRefPointerCollection@VCInstance@@@@0PAVMethodContext@@@Z
---

# CWbemProviderGlue::GetAllInstances


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/wbemglue/nl-wbemglue-cwbemproviderglue">CWbemProviderGlue</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetAllInstances</b> method retrieves a list of instances returned by a specific class.

## -parameters

### -param pszClassName

Name of class for which a list of instances should be returned.

### -param pList

Linked list of instances supported by the provider specified by <i>pszClassName</i>.

### -param pszNamespace

Namespace of the provider specified by <i>pszClassName</i>. This parameter can be <b>NULL</b> to indicate the default namespace, which is "Root\CIMv2".

### -param pMethodContext

Pointer to the current context. A context must be provided to prevent deadlocks. Either use the context passed into the provider by <a href="/windows/desktop/api/provider/nf-provider-provider-enumerateinstances">Provider::EnumerateInstances</a> or <a href="/windows/desktop/api/provider/nf-provider-provider-execquery">Provider::ExecQuery</a>, or else obtain it from the instance using <a href="/windows/desktop/api/instance/nf-instance-cinstance-getmethodcontext">CInstance::GetMethodContext</a>. This parameter must not be <b>NULL</b>.

## -returns

The method returns <b>WBEM_S_NO_ERROR</b> if the operation was successful, <b>WBEM_E_OUT_OF_MEMORY</b> if the operation failed due to lack of memory, or any other <b>HRESULT</b> error code.

## -remarks

The <b>GetAllInstances</b> method allows framework providers to access data from another provider without having to make a WMI API call. Framework providers pass the name of the provider to <b>GetAllInstances</b>, which returns a list of all of the instances that the provider supports.

This method is semantically equivalent to the query SELECT * FROM <i>pszBaseClassName</i> WHERE __Class = <i>pszBaseClassName</i>.