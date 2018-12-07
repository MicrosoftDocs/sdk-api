---
UID: NF:wbemglue.CWbemProviderGlue.GetInstancesByQuery(LPCWSTR,TRefPointerCollection<CInstance>,MethodContext,LPCWSTR)
title: CWbemProviderGlue::GetInstancesByQuery(LPCWSTR,TRefPointerCollection<CInstance>,MethodContext,LPCWSTR)
author: windows-sdk-content
description: The GetInstancesByQuery method retrieves a list of instances that match a particular query.
old-location: wmi\cwbemproviderglue_getinstancesbyquery.htm
tech.root: WmiSdk
ms.assetid: cf086577-8964-4b6b-8863-78b53f73397e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CWbemProviderGlue interface [Windows Management Instrumentation],GetInstancesByQuery method, CWbemProviderGlue.GetInstancesByQuery, CWbemProviderGlue.GetInstancesByQuery(LPCWSTR,TRefPointerCollection<CInstance>,MethodContext,LPCWSTR), CWbemProviderGlue::GetInstancesByQuery, CWbemProviderGlue::GetInstancesByQuery(LPCWSTR,TRefPointerCollection<CInstance>,MethodContext,LPCWSTR), GetInstancesByQuery, GetInstancesByQuery method [Windows Management Instrumentation], GetInstancesByQuery method [Windows Management Instrumentation],CWbemProviderGlue interface, _hmm_cwbemproviderglue_getinstancesbyquery, wbemglue/CWbemProviderGlue::GetInstancesByQuery, wmi.cwbemproviderglue_getinstancesbyquery
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CWbemProviderGlue::GetInstancesByQuery(LPCWSTR,TRefPointerCollection<CInstance>,MethodContext,LPCWSTR)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/493027c2-e54d-4fad-9e33-98d1ceab8860">CWbemProviderGlue</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetInstancesByQuery</b> method retrieves a list of instances that match a particular query.


## -parameters




### -param query

Query to be executed.


### -param pList

Linked list of instances that match the query specified by <i>Query</i>.


### -param pMethodContext

Pointer to the current context. A context must be provided to prevent deadlocks. Either use the context passed into the provider by <a href="https://msdn.microsoft.com/9566acb0-d7bf-4d3d-b7da-5cfbce150a2c">Provider::EnumerateInstances</a> or <a href="https://msdn.microsoft.com/94d5c8ee-2d61-42af-9a22-cc0df423b245">Provider::ExecQuery</a>, or else obtain it from the instance using <a href="https://msdn.microsoft.com/a2033754-4fd0-405f-9ad9-737eb8931016">CInstance::GetMethodContext</a>. This parameter must not be <b>NULL</b>.


### -param pszNamespace

Pointer to the namespace that contains the instances. If <b>NULL</b>, the default namespace, root<b>\</b>cimv2, is used.


## -returns



The method returns <b>WBEM_S_NO_ERROR</b> if the operation was successful, <b>WBEM_E_FAILED</b> if the operation failed, or any other <b>HRESULT</b> error code.




## -remarks



The <b>GetInstancesByQuery</b> method allows framework providers to access data from other providers without having to make a WMI API call. Framework providers pass a query to <b>GetInstancesByQuery</b>, which returns the appropriate instances.

For performance reasons, when calling this function, specify only the properties you need (for example, specify "SELECT <i>name</i>" instead of "SELECT *").



