---
UID: NF:wbemglue.CWbemProviderGlue.FrameworkLoginDLL(LPCWSTR,PLONG)
title: CWbemProviderGlue::FrameworkLoginDLL(LPCWSTR,PLONG)
author: windows-sdk-content
description: The FrameworkLoginDLL method is called when the DLL_PROCESS_ATTACH value is sent to DllMain to determine whether the provider server can be loaded.
old-location: wmi\cwbemproviderglue_frameworklogindll.htm
old-project: WmiSdk
ms.assetid: b701c70a-73f6-48b7-ab90-bbde1d29c9a2
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "?FrameworkLoginDLL@CWbemProviderGlue@@SAHPEBG@Z, ?FrameworkLoginDLL@CWbemProviderGlue@@SGHPBG@Z, CWbemProviderGlue interface [Windows Management Instrumentation],FrameworkLoginDLL method, CWbemProviderGlue.FrameworkLoginDLL, CWbemProviderGlue.FrameworkLoginDLL(LPCWSTR,PLONG), CWbemProviderGlue::FrameworkLoginDLL, CWbemProviderGlue::FrameworkLoginDLL(LPCWSTR,PLONG), FrameworkLoginDLL, FrameworkLoginDLL method [Windows Management Instrumentation], FrameworkLoginDLL method [Windows Management Instrumentation],CWbemProviderGlue interface, _hmm_cwbemproviderglue_frameworklogindll, wbemglue/CWbemProviderGlue::FrameworkLoginDLL, wmi.cwbemproviderglue_frameworklogindll"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CWbemProviderGlue.FrameworkLoginDLL
 - ?FrameworkLoginDLL@CWbemProviderGlue@@SAHPEBG@Z
 - ?FrameworkLoginDLL@CWbemProviderGlue@@SGHPBG@Z
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CWbemProviderGlue::FrameworkLoginDLL(LPCWSTR,PLONG)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/493027c2-e54d-4fad-9e33-98d1ceab8860">CWbemProviderGlue</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>FrameworkLoginDLL</b> method is called when the DLL_PROCESS_ATTACH value is sent to DllMain to determine whether the provider server can be loaded.


## -parameters




### -param name

Name of the server that is loaded.


### -param plRefCount






## -returns



The method returns <b>TRUE</b> if the server can be loaded and <b>FALSE</b> if the server cannot be loaded.




## -remarks



The <b>FrameworkLoginDLL</b> method should be called from DllMain when the <i>fdwReason</i> parameter has the value DLL_PROCESS_ATTACH. If <b>FrameworkLoginDLL</b> returns <b>FALSE</b>, the server should return <b>FALSE</b> from DllMain to fail the load.



