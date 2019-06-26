---
UID: NF:thrdbase.CThreadBase.BeginRead
title: CThreadBase::BeginRead (thrdbase.h)
author: windows-sdk-content
description: The BeginRead method provides thread safety by indicating the beginning of a data read operation when the provider is built on the WMI Provider Framework. CThreadBase is called internally.
old-location: wmi\cthreadbase_beginread.htm
tech.root: WmiSdk
ms.assetid: b5c4f714-b411-4a5f-af2b-0bf7ce3c9e70
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "?BeginRead@CThreadBase@@QAEHK@Z, BeginRead, BeginRead method [Windows Management Instrumentation], BeginRead method [Windows Management Instrumentation],CThreadBase interface, CThreadBase interface [Windows Management Instrumentation],BeginRead method, CThreadBase.BeginRead, CThreadBase::BeginRead, thrdbase/CThreadBase::BeginRead, wmi.cthreadbase_beginread"
ms.topic: method
f1_keywords: 
 - "thrdbase/CThreadBase.BeginRead"
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
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CThreadBase.BeginRead
 - ?BeginRead@CThreadBase@@QAEHK@Z
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CThreadBase::BeginRead


## -description


<p class="CCE_Message">[The <a href="https://docs.microsoft.com/windows/desktop/api/thrdbase/nl-thrdbase-cthreadbase">CThreadBase</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>BeginRead</b> method provides thread safety by indicating the beginning of a data read operation when the provider is built on the WMI Provider Framework. <a href="https://docs.microsoft.com/windows/desktop/api/thrdbase/nl-thrdbase-cthreadbase">CThreadBase</a> is called internally.


## -parameters




### -param dwTimeOut

Time-out for the read data operation. The default is no time-out.


## -returns



This method does not return a value.



