---
UID: NF:wbemglue.CWbemProviderGlue.GetInstanceByPath(LPCWSTR,CInstance,MethodContext)
title: CWbemProviderGlue::GetInstanceByPath(LPCWSTR,CInstance,MethodContext)
author: windows-sdk-content
description: The GetInstanceByPath method retrieves the instance identified by a particular object path by calling the provider GetObject method.
old-location: wmi\cwbemproviderglue_getinstancebypath.htm
tech.root: WmiSdk
ms.assetid: 788b5f5f-b300-4c86-afbd-416b938f21c1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "?GetInstanceByPath@CWbemProviderGlue@@SAJPEBGPEAPEAVCInstance@@PEAVMethodContext@@@Z, ?GetInstanceByPath@CWbemProviderGlue@@SGJPBGPAPAVCInstance@@PAVMethodContext@@@Z, CWbemProviderGlue interface [Windows Management Instrumentation],GetInstanceByPath method, CWbemProviderGlue.GetInstanceByPath, CWbemProviderGlue.GetInstanceByPath(LPCWSTR,CInstance,MethodContext), CWbemProviderGlue::GetInstanceByPath, CWbemProviderGlue::GetInstanceByPath(LPCWSTR,CInstance,MethodContext), GetInstanceByPath, GetInstanceByPath method [Windows Management Instrumentation], GetInstanceByPath method [Windows Management Instrumentation],CWbemProviderGlue interface, _hmm_cwbemproviderglue_getinstancebypath, wbemglue/CWbemProviderGlue::GetInstanceByPath, wmi.cwbemproviderglue_getinstancebypath"
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
 - CWbemProviderGlue.GetInstanceByPath
 - ?GetInstanceByPath@CWbemProviderGlue@@SAJPEBGPEAPEAVCInstance@@PEAVMethodContext@@@Z
 - ?GetInstanceByPath@CWbemProviderGlue@@SGJPBGPAPAVCInstance@@PAVMethodContext@@@Z
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CWbemProviderGlue::GetInstanceByPath(LPCWSTR,CInstance,MethodContext)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/493027c2-e54d-4fad-9e33-98d1ceab8860">CWbemProviderGlue</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetInstanceByPath</b> method 
    retrieves the instance identified by a particular object path by calling the provider 
    <a href="https://msdn.microsoft.com/c8e2633a-cbea-422c-9598-1b1b1104bbc2">GetObject</a> method.


## -parameters




### -param pszObjectPath

An object path to the instance to be returned.


### -param ppInstance

A pointer to a pointer to a <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> instance used to 
      store the new instance. The framework provider that performs the request must release this pointer.


### -param pMethodContext

A pointer to the current context. A context must be provided to prevent deadlocks. Either use the context 
      passed into the provider by 
      <a href="https://msdn.microsoft.com/9566acb0-d7bf-4d3d-b7da-5cfbce150a2c">Provider::EnumerateInstances</a> or 
      <a href="https://msdn.microsoft.com/94d5c8ee-2d61-42af-9a22-cc0df423b245">Provider::ExecQuery</a>, or else obtain it from the 
      instance using <a href="https://msdn.microsoft.com/a2033754-4fd0-405f-9ad9-737eb8931016">CInstance::GetMethodContext</a>. 
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
    <a href="https://msdn.microsoft.com/9566acb0-d7bf-4d3d-b7da-5cfbce150a2c">Provider::EnumerateInstances</a> or 
    <a href="https://msdn.microsoft.com/94d5c8ee-2d61-42af-9a22-cc0df423b245">Provider::ExecQuery</a>, or else obtain it from the 
    instance using 
    <a href="https://msdn.microsoft.com/a2033754-4fd0-405f-9ad9-737eb8931016">CInstance::GetMethodContext</a>.



