---
UID: NF:thrdbase.CThreadBase.EndRead
title: CThreadBase::EndRead (thrdbase.h)
description: The EndRead method provides thread safety by indicating the end of a data read operation when the provider is built on the WMI Provider Framework. CThreadBase is called internally.
helpviewer_keywords: ["?EndRead@CThreadBase@@QAEXXZ","CThreadBase interface [Windows Management Instrumentation]","EndRead method","CThreadBase.EndRead","CThreadBase::EndRead","EndRead","EndRead method [Windows Management Instrumentation]","EndRead method [Windows Management Instrumentation]","CThreadBase interface","thrdbase/CThreadBase::EndRead","wmi.cthreadbase_endread"]
old-location: wmi\cthreadbase_endread.htm
tech.root: wmi
ms.assetid: e34fa8bc-f667-4fca-9282-9ca8038f3e75
ms.date: 12/05/2018
ms.keywords: ?EndRead@CThreadBase@@QAEXXZ, CThreadBase interface [Windows Management Instrumentation],EndRead method, CThreadBase.EndRead, CThreadBase::EndRead, EndRead, EndRead method [Windows Management Instrumentation], EndRead method [Windows Management Instrumentation],CThreadBase interface, thrdbase/CThreadBase::EndRead, wmi.cthreadbase_endread
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
 - CThreadBase::EndRead
 - thrdbase/CThreadBase::EndRead
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
 - CThreadBase.EndRead
 - ?EndRead@CThreadBase@@QAEXXZ
---

# CThreadBase::EndRead


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/thrdbase/nl-thrdbase-cthreadbase">CThreadBase</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>EndRead</b> method provides thread safety by indicating the end of a data read operation when the provider is built on the WMI Provider Framework.  <a href="/windows/desktop/api/thrdbase/nl-thrdbase-cthreadbase">CThreadBase</a> is called internally.


