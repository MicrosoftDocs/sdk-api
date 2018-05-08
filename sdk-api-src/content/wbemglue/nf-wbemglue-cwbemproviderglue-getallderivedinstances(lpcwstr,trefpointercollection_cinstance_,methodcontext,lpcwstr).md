---
UID: NF:wbemglue.CWbemProviderGlue.GetAllDerivedInstances(LPCWSTR,TRefPointerCollection<CInstance>,MethodContext,LPCWSTR)
title: CWbemProviderGlue::GetAllDerivedInstances(LPCWSTR,TRefPointerCollection<CInstance>,MethodContext,LPCWSTR)
author: windows-driver-content
description: The GetAllDerivedInstances method retrieves a list of instances of a base class, or any children of that base class.
old-location: wmi\cwbemproviderglue_getallderivedinstances.htm
old-project: WmiSdk
ms.assetid: ecdca316-12a0-46c3-97df-85a087533837
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: CWbemProviderGlue interface [Windows Management Instrumentation],GetAllDerivedInstances method, CWbemProviderGlue.GetAllDerivedInstances, CWbemProviderGlue.GetAllDerivedInstances(LPCWSTR,TRefPointerCollection<CInstance>,MethodContext,LPCWSTR), CWbemProviderGlue::GetAllDerivedInstances, CWbemProviderGlue::GetAllDerivedInstances(LPCWSTR,TRefPointerCollection<CInstance>,MethodContext,LPCWSTR), GetAllDerivedInstances, GetAllDerivedInstances method [Windows Management Instrumentation], GetAllDerivedInstances method [Windows Management Instrumentation],CWbemProviderGlue interface, _hmm_cwbemproviderglue_getallderivedinstances, wbemglue/CWbemProviderGlue::GetAllDerivedInstances, wmi.cwbemproviderglue_getallderivedinstances
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
req.typenames: WbemTimeout
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FrameDynOS.dll
-	FrameDyn.dll
api_name:
-	CWbemProviderGlue.GetAllDerivedInstances
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CWbemProviderGlue::GetAllDerivedInstances(LPCWSTR,TRefPointerCollection<CInstance>,MethodContext,LPCWSTR)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/493027c2-e54d-4fad-9e33-98d1ceab8860">CWbemProviderGlue</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetAllDerivedInstances</b> method retrieves a list of instances of a base class, or any children of that base class.


## -parameters




### -param pszBaseClassName

Pointer to name of base class for which list should be returned.


### -param pList

Pointer to linked list of instances derived from the class specified by <i>pszBaseClassName</i>.


### -param pMethodContext

Pointer to the current context. A context must be provided to prevent deadlocks. Either use the context passed into the provider by <a href="https://msdn.microsoft.com/9566acb0-d7bf-4d3d-b7da-5cfbce150a2c">Provider::EnumerateInstances</a> or <a href="https://msdn.microsoft.com/94d5c8ee-2d61-42af-9a22-cc0df423b245">Provider::ExecQuery</a>, or else obtain it from the instance using <a href="https://msdn.microsoft.com/a2033754-4fd0-405f-9ad9-737eb8931016">CInstance::GetMethodContext</a>. This parameter must not be <b>NULL</b>.


### -param pszNamespace

Namespace of the class name specified by <i>pszBaseClassName</i>. When this parameter is <b>NULL</b>, the default namespace root\cimv2 is used.


## -returns



The method returns <b>WBEM_S_NO_ERROR</b> if the operation was successful, <b>WBEM_E_OUT_OF_MEMORY</b> if the operation failed due to lack of memory, or any other <b>HRESULT</b> error code.




## -remarks



The <b>GetAllDerivedInstances</b> method allows framework providers to access data from other providers. Framework providers pass the name of a base class to <b>GetAllDerivedInstances</b>, which returns a list of all of the instances that derive from it.

The return codes include all the possible returns from <a href="https://msdn.microsoft.com/8cb4a42b-f8ae-4a6f-884c-fa808b11dc8a">IWbemServices::ExecQuery</a>.

This method is semantically equivalent to the query SELECT * FROM <i>pszBaseClassName</i>.



