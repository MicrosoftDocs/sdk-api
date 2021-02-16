---
UID: NF:thrdbase.CThreadBase.CThreadBase
title: CThreadBase::CThreadBase (thrdbase.h)
description: The CThreadBase::CThreadBase constructor initializes a new instance of CThreadBase. CThreadBase is called internally.
helpviewer_keywords: ["??0CThreadBase@@QAE@W4THREAD_SAFETY_MECHANISM@0@@Z","CThreadBase","CThreadBase interface [Windows Management Instrumentation]","CThreadBase method","CThreadBase method [Windows Management Instrumentation]","CThreadBase method [Windows Management Instrumentation]","CThreadBase interface","CThreadBase.CThreadBase","CThreadBase::CThreadBase","thrdbase/CThreadBase::CThreadBase","wmi.cthreadbase_cthreadbase"]
old-location: wmi\cthreadbase_cthreadbase.htm
tech.root: wmi
ms.assetid: 43909501-0a65-4728-9a26-30b8391a33c5
ms.date: 12/05/2018
ms.keywords: ??0CThreadBase@@QAE@W4THREAD_SAFETY_MECHANISM@0@@Z, CThreadBase, CThreadBase interface [Windows Management Instrumentation],CThreadBase method, CThreadBase method [Windows Management Instrumentation], CThreadBase method [Windows Management Instrumentation],CThreadBase interface, CThreadBase.CThreadBase, CThreadBase::CThreadBase, thrdbase/CThreadBase::CThreadBase, wmi.cthreadbase_cthreadbase
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CThreadBase::CThreadBase
 - thrdbase/CThreadBase::CThreadBase
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CThreadBase.CThreadBase
 - ??0CThreadBase@@QAE@W4THREAD_SAFETY_MECHANISM@0@@Z
---

# CThreadBase::CThreadBase


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/thrdbase/nl-thrdbase-cthreadbase">CThreadBase</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>CThreadBase::CThreadBase</b>  constructor initializes a new instance of <a href="/windows/desktop/api/thrdbase/nl-thrdbase-cthreadbase">CThreadBase</a>. <b>CThreadBase</b> is called internally.

## -parameters

### -param etsm

The thread safety mechanism. The possible values are:

<b>etsmFirst</b>
<b>etsmSerialized</b>
<b>etsmPriorityRead</b>
<b>etsmPriorityWrite</b>
<b>etsmLast</b>

## -remarks

The destructor for the class is <b>CThreadBase::~CThreadBase</b>.