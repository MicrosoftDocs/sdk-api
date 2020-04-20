---
UID: NF:wbemglue.CWbemProviderGlue.FrameworkLoginDLL(LPCWSTR,PLONG)
title: CWbemProviderGlue::FrameworkLoginDLL(LPCWSTR,PLONG) (wbemglue.h)
description: The FrameworkLoginDLL method is called when the DLL_PROCESS_ATTACH value is sent to DllMain to determine whether the provider server can be loaded.helpviewer_keywords: ["?FrameworkLoginDLL@CWbemProviderGlue@@SAHPEBG@Z","?FrameworkLoginDLL@CWbemProviderGlue@@SGHPBG@Z","CWbemProviderGlue interface [Windows Management Instrumentation]","FrameworkLoginDLL method","CWbemProviderGlue.FrameworkLoginDLL","CWbemProviderGlue.FrameworkLoginDLL(LPCWSTR","PLONG)","CWbemProviderGlue::FrameworkLoginDLL","CWbemProviderGlue::FrameworkLoginDLL(LPCWSTR","PLONG)","FrameworkLoginDLL","FrameworkLoginDLL method [Windows Management Instrumentation]","FrameworkLoginDLL method [Windows Management Instrumentation]","CWbemProviderGlue interface","_hmm_cwbemproviderglue_frameworklogindll","wbemglue/CWbemProviderGlue::FrameworkLoginDLL","wmi.cwbemproviderglue_frameworklogindll"]
old-location: wmi\cwbemproviderglue_frameworklogindll.htm
tech.root: WmiSdk
ms.assetid: b701c70a-73f6-48b7-ab90-bbde1d29c9a2
ms.date: 12/05/2018
ms.keywords: ?FrameworkLoginDLL@CWbemProviderGlue@@SAHPEBG@Z, ?FrameworkLoginDLL@CWbemProviderGlue@@SGHPBG@Z, CWbemProviderGlue interface [Windows Management Instrumentation],FrameworkLoginDLL method, CWbemProviderGlue.FrameworkLoginDLL, CWbemProviderGlue.FrameworkLoginDLL(LPCWSTR,PLONG), CWbemProviderGlue::FrameworkLoginDLL, CWbemProviderGlue::FrameworkLoginDLL(LPCWSTR,PLONG), FrameworkLoginDLL, FrameworkLoginDLL method [Windows Management Instrumentation], FrameworkLoginDLL method [Windows Management Instrumentation],CWbemProviderGlue interface, _hmm_cwbemproviderglue_frameworklogindll, wbemglue/CWbemProviderGlue::FrameworkLoginDLL, wmi.cwbemproviderglue_frameworklogindll
f1_keywords:
- wbemglue/CWbemProviderGlue.FrameworkLoginDLL
dev_langs:
- c++
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
- CWbemProviderGlue.FrameworkLoginDLL
- ?FrameworkLoginDLL@CWbemProviderGlue@@SAHPEBG@Z
- ?FrameworkLoginDLL@CWbemProviderGlue@@SGHPBG@Z
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CWbemProviderGlue::FrameworkLoginDLL(LPCWSTR,PLONG)


## -description


<p class="CCE_Message">[The <a href="https://docs.microsoft.com/windows/desktop/api/wbemglue/nl-wbemglue-cwbemproviderglue">CWbemProviderGlue</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>FrameworkLoginDLL</b> method is called when the DLL_PROCESS_ATTACH value is sent to DllMain to determine whether the provider server can be loaded.


## -parameters




### -param name

Name of the server that is loaded.


### -param plRefCount

The current reference count. This LONG must be the same one used in FrameworkLoginDLL and as the parameter to the CWbemGlueFactory constructor.





## -returns



The method returns <b>TRUE</b> if the server can be loaded and <b>FALSE</b> if the server cannot be loaded.




## -remarks



The <b>FrameworkLoginDLL</b> method should be called from DllMain when the <i>fdwReason</i> parameter has the value DLL_PROCESS_ATTACH. If <b>FrameworkLoginDLL</b> returns <b>FALSE</b>, the server should return <b>FALSE</b> from DllMain to fail the load.



