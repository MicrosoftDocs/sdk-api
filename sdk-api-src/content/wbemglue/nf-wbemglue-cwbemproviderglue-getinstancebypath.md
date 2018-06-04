---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# CWbemProviderGlue::GetInstanceByPath


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


#### - pszInstancePath

An object path to the instance to be returned.


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



