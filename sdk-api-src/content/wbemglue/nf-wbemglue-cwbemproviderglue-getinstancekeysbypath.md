---
UID: NF:wbemglue.CWbemProviderGlue.GetInstanceKeysByPath
title: CWbemProviderGlue::GetInstanceKeysByPath method
author: windows-driver-content
description: The GetInstanceKeysByPath method retrieves the instance identified by a particular object path, with only the key properties populated.
old-location: wmi\cwbemproviderglue_getinstancekeysbypath.htm
old-project: WmiSdk
ms.assetid: 8ae95850-59e9-4382-b88d-c51eb3077176
ms.author: windowsdriverdev
ms.date: 3/16/2018
ms.keywords: CWbemProviderGlue, CWbemProviderGlue interface [Windows Management Instrumentation], GetInstanceKeysByPath method, CWbemProviderGlue::GetInstanceKeysByPath, GetInstanceKeysByPath method [Windows Management Instrumentation], GetInstanceKeysByPath method [Windows Management Instrumentation], CWbemProviderGlue interface, GetInstanceKeysByPath,CWbemProviderGlue.GetInstanceKeysByPath, _hmm_cwbemproviderglue_getinstancekeysbypath, wbemglue/CWbemProviderGlue::GetInstanceKeysByPath, wmi.cwbemproviderglue_getinstancekeysbypath
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
-	CWbemProviderGlue.GetInstanceKeysByPath
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CWbemProviderGlue::GetInstanceKeysByPath method


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/493027c2-e54d-4fad-9e33-98d1ceab8860">CWbemProviderGlue</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetInstanceKeysByPath</b> method retrieves the instance identified by a particular object path, with only the key properties populated.


## -parameters




### -param pszInstancePath

An object path to the instance to be returned.


### -param ppInstance

A pointer to a pointer to a new <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> instance whose keys are those specified in the <i>pszInstancePath</i>. The framework provider the performs the request must release this pointer.


### -param pMethodContext

A pointer to the current context. A context must be provided to prevent deadlocks. Either use the context passed into the provider by <a href="https://msdn.microsoft.com/9566acb0-d7bf-4d3d-b7da-5cfbce150a2c">Provider::EnumerateInstances</a> or <a href="https://msdn.microsoft.com/94d5c8ee-2d61-42af-9a22-cc0df423b245">Provider::ExecQuery</a>, or else obtain it from the instance using <a href="https://msdn.microsoft.com/a2033754-4fd0-405f-9ad9-737eb8931016">CInstance::GetMethodContext</a>. This parameter must not be <b>NULL</b>.


## -returns



Returns <b>WBEM_S_NO_ERROR</b> if the operation was successful, <b>WBEM_E_OUT_OF_MEMORY</b> if the operation failed due to lack of memory, or any other <b>HRESULT</b> error code.




## -remarks



This method makes use of partial-instance update operations to request only the key properties of the specified object. It is the most efficient way to verify the existence of a specific object. Be aware that not all providers support partial-instance operations. In that case, the entire instance will be populated. For more information, see <a href="https://msdn.microsoft.com/bc498655-ad6d-44f5-912d-9b7ee95825ec">Supporting Partial-Instance Operations</a>.

In the current version of the provider framework, <i>pszInstancePath</i> must resolve to be an instance path on the same computer.




## -see-also




<a href="https://msdn.microsoft.com/493027c2-e54d-4fad-9e33-98d1ceab8860">CWbemProviderGlue</a>



<a href="https://msdn.microsoft.com/788b5f5f-b300-4c86-afbd-416b938f21c1">GetInstanceByPath</a>



<a href="https://msdn.microsoft.com/d9232dc0-6df9-440d-bf7a-bf524acbe505">GetInstancePropertiesByPath</a>
 

 

