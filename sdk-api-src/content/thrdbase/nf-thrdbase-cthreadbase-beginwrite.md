---
UID: NF:thrdbase.CThreadBase.BeginWrite
title: CThreadBase::BeginWrite (thrdbase.h)
description: The BeginWrite method provides thread safety by indicating the beginning of a data write operation when the provider is built on the WMI Provider Framework. CThreadBase is called internally.
helpviewer_keywords: ["?BeginWrite@CThreadBase@@QAEHK@Z","BeginWrite","BeginWrite method [Windows Management Instrumentation]","BeginWrite method [Windows Management Instrumentation]","CThreadBase interface","CThreadBase interface [Windows Management Instrumentation]","BeginWrite method","CThreadBase.BeginWrite","CThreadBase::BeginWrite","thrdbase/CThreadBase::BeginWrite","wmi.cthreadbase_beginwrite"]
old-location: wmi\cthreadbase_beginwrite.htm
tech.root: wmi
ms.assetid: 51ae6b39-b524-4bf9-ac71-45c812ad1680
ms.date: 12/05/2018
ms.keywords: ?BeginWrite@CThreadBase@@QAEHK@Z, BeginWrite, BeginWrite method [Windows Management Instrumentation], BeginWrite method [Windows Management Instrumentation],CThreadBase interface, CThreadBase interface [Windows Management Instrumentation],BeginWrite method, CThreadBase.BeginWrite, CThreadBase::BeginWrite, thrdbase/CThreadBase::BeginWrite, wmi.cthreadbase_beginwrite
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
 - CThreadBase::BeginWrite
 - thrdbase/CThreadBase::BeginWrite
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
 - CThreadBase.BeginWrite
 - ?BeginWrite@CThreadBase@@QAEHK@Z
---

# CThreadBase::BeginWrite


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/thrdbase/nl-thrdbase-cthreadbase">CThreadBase</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>BeginWrite</b> method provides thread safety by indicating the beginning of a data write operation when the provider is built on the WMI Provider Framework. <a href="/windows/desktop/api/thrdbase/nl-thrdbase-cthreadbase">CThreadBase</a> is called internally.

## -parameters

### -param dwTimeOut

Timeout for the write data operation. The default is no timeout.

## -returns

This method does not return a value.