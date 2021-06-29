---
UID: NF:instance.CInstance.GetMethodContext
title: CInstance::GetMethodContext (instance.h)
description: The GetMethodContext method returns a pointer to a MethodContext object.
helpviewer_keywords: ["?GetMethodContext@CInstance@@QBEPAVMethodContext@@XZ","?GetMethodContext@CInstance@@QEBAPEAVMethodContext@@XZ","CInstance interface [Windows Management Instrumentation]","GetMethodContext method","CInstance.GetMethodContext","CInstance::GetMethodContext","GetMethodContext","GetMethodContext method [Windows Management Instrumentation]","GetMethodContext method [Windows Management Instrumentation]","CInstance interface","_hmm_cinstance_getmethodcontext","instance/CInstance::GetMethodContext","wmi.cinstance_getmethodcontext"]
old-location: wmi\cinstance_getmethodcontext.htm
tech.root: wmi
ms.assetid: a2033754-4fd0-405f-9ad9-737eb8931016
ms.date: 12/05/2018
ms.keywords: ?GetMethodContext@CInstance@@QBEPAVMethodContext@@XZ, ?GetMethodContext@CInstance@@QEBAPEAVMethodContext@@XZ, CInstance interface [Windows Management Instrumentation],GetMethodContext method, CInstance.GetMethodContext, CInstance::GetMethodContext, GetMethodContext, GetMethodContext method [Windows Management Instrumentation], GetMethodContext method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_getmethodcontext, instance/CInstance::GetMethodContext, wmi.cinstance_getmethodcontext
req.header: instance.h
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
 - CInstance::GetMethodContext
 - instance/CInstance::GetMethodContext
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
 - CInstance.GetMethodContext
 - ?GetMethodContext@CInstance@@QBEPAVMethodContext@@XZ
 - ?GetMethodContext@CInstance@@QEBAPEAVMethodContext@@XZ
---

# CInstance::GetMethodContext


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetMethodContext</b> method returns a pointer to a <b>MethodContext</b> object.



## -returns

Returns a pointer to the current <b>MethodContext</b> object.

## -remarks

Framework providers should not release the <b>MethodContext</b> pointer returned by this function.
