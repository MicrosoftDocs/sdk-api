---
UID: NF:provider.Provider.GetLocalComputerName
title: Provider::GetLocalComputerName (provider.h)
author: windows-sdk-content
description: The GetLocalComputerName method returns a constant reference to the computer name in CHString format.
old-location: wmi\provider_getlocalcomputername.htm
tech.root: WmiSdk
ms.assetid: 20470353-417d-4067-8df1-c2ec6b330853
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetLocalComputerName, GetLocalComputerName method [Windows Management Instrumentation], GetLocalComputerName method [Windows Management Instrumentation],Provider interface, Provider interface [Windows Management Instrumentation],GetLocalComputerName method, Provider.GetLocalComputerName, Provider::GetLocalComputerName, _hmm_provider_getlocalcomputername, provider/Provider::GetLocalComputerName, wmi.provider_getlocalcomputername
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
 - Provider.GetLocalComputerName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Provider::GetLocalComputerName


## -description


<p class="CCE_Message">[The <a href="https://docs.microsoft.com/windows/desktop/api/provider/nl-provider-provider">Provider</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetLocalComputerName</b> method returns a constant reference to the computer name in <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/chstring">CHString</a> format.


## -parameters






## -returns



Returns a constant reference to the name of the computer.



