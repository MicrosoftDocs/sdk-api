---
UID: NF:thrdbase.CThreadBase.EndWrite
title: CThreadBase::EndWrite (thrdbase.h)
description: The EndWrite method provides thread safety by indicating the end of a data write operation when the provider is built on the WMI Provider Framework. CThreadBase is called internally.
helpviewer_keywords: ["?Empty@CHString@@QEAAXXZ","CThreadBase interface [Windows Management Instrumentation]","EndWrite method","CThreadBase.EndWrite","CThreadBase::EndWrite","EndWrite","EndWrite method [Windows Management Instrumentation]","EndWrite method [Windows Management Instrumentation]","CThreadBase interface","thrdbase/CThreadBase::EndWrite","wmi.cthreadbase_endwrite"]
old-location: wmi\cthreadbase_endwrite.htm
tech.root: wmi
ms.assetid: 8b57bcc0-f8ca-412a-87d9-9afeb5ac8446
ms.date: 12/05/2018
ms.keywords: ?Empty@CHString@@QEAAXXZ, CThreadBase interface [Windows Management Instrumentation],EndWrite method, CThreadBase.EndWrite, CThreadBase::EndWrite, EndWrite, EndWrite method [Windows Management Instrumentation], EndWrite method [Windows Management Instrumentation],CThreadBase interface, thrdbase/CThreadBase::EndWrite, wmi.cthreadbase_endwrite
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
 - CThreadBase::EndWrite
 - thrdbase/CThreadBase::EndWrite
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
 - CThreadBase.EndWrite
 - ?Empty@CHString@@QEAAXXZ
---

# CThreadBase::EndWrite


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/thrdbase/nl-thrdbase-cthreadbase">CThreadBase</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>EndWrite</b> method provides thread safety by indicating the end of a data write operation when the provider is built on the WMI Provider Framework. <a href="/windows/desktop/api/thrdbase/nl-thrdbase-cthreadbase">CThreadBase</a> is called internally.


