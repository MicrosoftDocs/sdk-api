---
UID: NF:thrdbase.CThreadBase.OnFinalRelease
title: CThreadBase::OnFinalRelease (thrdbase.h)
description: The OnFinalRelease method is a virtual function called by Release when the reference count reaches zero. CThreadBase is called internally.
old-location: wmi\cthreadbase_onfinalrelease.htm
tech.root: WmiSdk
ms.assetid: a17a379d-60ba-4a76-8900-58fabadad5ea
ms.date: 12/05/2018
ms.keywords: ?OnFinalRelease@CThreadBase@@MAEXXZ, ?OnFinalRelease@CThreadBase@@MEAAXXZ, CThreadBase interface [Windows Management Instrumentation],OnFinalRelease method, CThreadBase.OnFinalRelease, CThreadBase::OnFinalRelease, OnFinalRelease, OnFinalRelease method [Windows Management Instrumentation], OnFinalRelease method [Windows Management Instrumentation],CThreadBase interface, thrdbase/CThreadBase::OnFinalRelease, wmi.cthreadbase_onfinalrelease
f1_keywords:
- thrdbase/CThreadBase.OnFinalRelease
dev_langs:
- c++
req.header: thrdbase.h
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
- DllExport
api_location:
- FrameDynOS.dll
- FrameDyn.dll
api_name:
- CThreadBase.OnFinalRelease
- ?OnFinalRelease@CThreadBase@@MAEXXZ
- ?OnFinalRelease@CThreadBase@@MEAAXXZ
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CThreadBase::OnFinalRelease


## -description


<p class="CCE_Message">[The <a href="https://docs.microsoft.com/windows/desktop/api/thrdbase/nl-thrdbase-cthreadbase">CThreadBase</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>OnFinalRelease</b>  method  is a virtual function called by <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> when the reference count reaches zero. <a href="https://docs.microsoft.com/windows/desktop/api/thrdbase/nl-thrdbase-cthreadbase">CThreadBase</a> is called internally.


## -parameters






## -returns



This method does not return a value.



