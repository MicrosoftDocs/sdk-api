---
UID: NF:wbemglue.CWbemProviderGlue.GetInstancesByQuery(LPCWSTR,TRefPointerCollection<CInstance>,MethodContext,LPCWSTR)~r1
title: CWbemProviderGlue::GetInstancesByQuery (wbemglue.h)
description: The CWbemProviderGlue::GetInstancesByQuery (wbemglue.h) method retrieves a list of instances that match a particular query.
helpviewer_keywords: ["CWbemProviderGlue interface [Windows Management Instrumentation]","GetInstancesByQuery method","CWbemProviderGlue.GetInstancesByQuery","CWbemProviderGlue::GetInstancesByQuery","GetInstancesByQuery","GetInstancesByQuery method [Windows Management Instrumentation]","GetInstancesByQuery method [Windows Management Instrumentation]","CWbemProviderGlue interface","_hmm_cwbemproviderglue_getinstancesbyquery","wbemglue/CWbemProviderGlue::GetInstancesByQuery","wmi.cwbemproviderglue_getinstancesbyquery"]
old-location: wmi\cwbemproviderglue_getinstancesbyquery.htm
tech.root: wmi
ms.assetid: cf086577-8964-4b6b-8863-78b53f73397e
ms.date: 08/15/2022
ms.keywords: CWbemProviderGlue interface [Windows Management Instrumentation],GetInstancesByQuery method, CWbemProviderGlue.GetInstancesByQuery, CWbemProviderGlue::GetInstancesByQuery, GetInstancesByQuery, GetInstancesByQuery method [Windows Management Instrumentation], GetInstancesByQuery method [Windows Management Instrumentation],CWbemProviderGlue interface, _hmm_cwbemproviderglue_getinstancesbyquery, wbemglue/CWbemProviderGlue::GetInstancesByQuery, wmi.cwbemproviderglue_getinstancesbyquery
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
 - CWbemProviderGlue::GetInstancesByQuery
 - wbemglue/CWbemProviderGlue::GetInstancesByQuery
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
 - CWbemProviderGlue.GetInstancesByQuery
---

# CWbemProviderGlue::GetInstancesByQuery


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/wbemglue/nl-wbemglue-cwbemproviderglue">CWbemProviderGlue</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetInstancesByQuery</b> method retrieves a list of instances that match a particular query.

## -parameters

### -param query

Query to be executed.

### -param pList

Linked list of instances that match the query specified by <i>Query</i>.

### -param pMethodContext

Pointer to the current context. A context must be provided to prevent deadlocks. Either use the context passed into the provider by <a href="/windows/desktop/api/provider/nf-provider-provider-enumerateinstances">Provider::EnumerateInstances</a> or <a href="/windows/desktop/api/provider/nf-provider-provider-execquery">Provider::ExecQuery</a>, or else obtain it from the instance using <a href="/windows/desktop/api/instance/nf-instance-cinstance-getmethodcontext">CInstance::GetMethodContext</a>. This parameter must not be <b>NULL</b>.

### -param pszNamespace

Pointer to the namespace that contains the instances. If <b>NULL</b>, the default namespace, root<b>\\</b>cimv2, is used.

## -returns

The method returns <b>WBEM_S_NO_ERROR</b> if the operation was successful, <b>WBEM_E_FAILED</b> if the operation failed, or any other <b>HRESULT</b> error code.

## -remarks

The <b>GetInstancesByQuery</b> method allows framework providers to access data from other providers without having to make a WMI API call. Framework providers pass a query to <b>GetInstancesByQuery</b>, which returns the appropriate instances.

For performance reasons, when calling this function, specify only the properties you need (for example, specify "SELECT <i>name</i>" instead of "SELECT *").