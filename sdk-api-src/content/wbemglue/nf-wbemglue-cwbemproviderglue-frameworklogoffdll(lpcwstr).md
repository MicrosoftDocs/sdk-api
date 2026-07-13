---
UID: NF:wbemglue.CWbemProviderGlue.FrameworkLogoffDLL(LPCWSTR)
title: CWbemProviderGlue::FrameworkLogoffDLL (wbemglue.h)
description: The FrameworkLogoffDLL method is called by DllCanUnloadNow to determine whether the provider server is not in use and can be unloaded. (overload 1/2)
helpviewer_keywords: ["?FrameworkLogoffDLL@CWbemProviderGlue@@SAHPEBG@Z","?FrameworkLogoffDLL@CWbemProviderGlue@@SGHPBG@Z","CWbemProviderGlue interface [Windows Management Instrumentation]","FrameworkLogoffDLL method","CWbemProviderGlue.FrameworkLogoffDLL","CWbemProviderGlue::FrameworkLogoffDLL","FrameworkLogoffDLL","FrameworkLogoffDLL method [Windows Management Instrumentation]","FrameworkLogoffDLL method [Windows Management Instrumentation]","CWbemProviderGlue interface","_hmm_cwbemproviderglue_frameworklogoffdll","wbemglue/CWbemProviderGlue::FrameworkLogoffDLL","wmi.cwbemproviderglue_frameworklogoffdll"]
old-location: wmi\cwbemproviderglue_frameworklogoffdll.htm
tech.root: wmi
ms.assetid: 5157d823-d3a1-46d2-8ae8-07e904001a14
ms.date: 12/05/2018
ms.keywords: ?FrameworkLogoffDLL@CWbemProviderGlue@@SAHPEBG@Z, ?FrameworkLogoffDLL@CWbemProviderGlue@@SGHPBG@Z, CWbemProviderGlue interface [Windows Management Instrumentation],FrameworkLogoffDLL method, CWbemProviderGlue.FrameworkLogoffDLL, CWbemProviderGlue::FrameworkLogoffDLL, FrameworkLogoffDLL, FrameworkLogoffDLL method [Windows Management Instrumentation], FrameworkLogoffDLL method [Windows Management Instrumentation],CWbemProviderGlue interface, _hmm_cwbemproviderglue_frameworklogoffdll, wbemglue/CWbemProviderGlue::FrameworkLogoffDLL, wmi.cwbemproviderglue_frameworklogoffdll
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
 - CWbemProviderGlue::FrameworkLogoffDLL
 - wbemglue/CWbemProviderGlue::FrameworkLogoffDLL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CWbemProviderGlue.FrameworkLogoffDLL
 - ?FrameworkLogoffDLL@CWbemProviderGlue@@SAHPEBG@Z
 - ?FrameworkLogoffDLL@CWbemProviderGlue@@SGHPBG@Z
---

# CWbemProviderGlue::FrameworkLogoffDLL


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/wbemglue/nl-wbemglue-cwbemproviderglue">CWbemProviderGlue</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>FrameworkLogoffDLL</b> method is called by <b>DllCanUnloadNow</b> to determine whether the provider server is not in use and can be unloaded.

## -parameters

### -param name

Name of the server that is unloaded.

## -returns

The method returns <b>TRUE</b> if the server is not in use and can be unloaded and <b>FALSE</b> if the server is still in use and cannot be unloaded.

## -remarks

For now,  <b>FrameworkLogoffDLL</b> returns <b>FALSE</b> until the refcount for <a href="/windows/desktop/api/wbemglue/nl-wbemglue-cwbemproviderglue">CWbemProviderGlue</a> is zero. This approach prevents unloading any client DLL while instances of <b>CWbemProviderGlue</b> still exist.
