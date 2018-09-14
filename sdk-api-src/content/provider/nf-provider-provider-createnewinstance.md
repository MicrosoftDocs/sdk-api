---
UID: NF:provider.Provider.CreateNewInstance
title: Provider::CreateNewInstance
author: windows-sdk-content
description: The CreateNewInstance method allocates a new CInstance object and returns a pointer to it.
old-location: wmi\provider_createnewinstance.htm
tech.root: WmiSdk
ms.assetid: cb520b55-9ef8-4f5a-935d-46c2bb01f5dd
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: "?CreateNewInstance@Provider@@IAEPAVCInstance@@PAVMethodContext@@@Z, ?CreateNewInstance@Provider@@IEAAPEAVCInstance@@PEAVMethodContext@@@Z, CreateNewInstance, CreateNewInstance method [Windows Management Instrumentation], CreateNewInstance method [Windows Management Instrumentation],Provider interface, Provider interface [Windows Management Instrumentation],CreateNewInstance method, Provider.CreateNewInstance, Provider::CreateNewInstance, _hmm_provider_createnewinstance, provider/Provider::CreateNewInstance, wmi.provider_createnewinstance"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: provider.h
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
 - Provider.CreateNewInstance
 - ?CreateNewInstance@Provider@@IAEPAVCInstance@@PAVMethodContext@@@Z
 - ?CreateNewInstance@Provider@@IEAAPEAVCInstance@@PEAVMethodContext@@@Z
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Provider::CreateNewInstance


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/d8a7c433-7e6a-45cc-914f-a15a3688c7aa">Provider</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>CreateNewInstance</b> method allocates a new <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> object and returns a pointer to it.


## -parameters




### -param pMethodContext

A pointer to the context associated with this instance.


## -returns



Returns a pointer to the new instance.




## -remarks



The caller must call either CInstance::Release or <a href="https://msdn.microsoft.com/619adf78-26db-4a90-90ba-bdacb3e55975">Provider::Commit</a> on the returned pointer. Either of these methods may be used, but they are not interchangeable. Refer to the Remarks section on each of these methods to determine which is appropriate.

This method does not return a <b>NULL</b> pointer. If it fails, it throws an exception.



