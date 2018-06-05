---
UID: NF:thrdbase.CThreadBase.BeginWrite
title: CThreadBase::BeginWrite
author: windows-sdk-content
description: The BeginWrite method provides thread safety by indicating the beginning of a data write operation when the provider is built on the WMI Provider Framework. CThreadBase is called internally.
old-location: wmi\cthreadbase_beginwrite.htm
old-project: WmiSdk
ms.assetid: 51ae6b39-b524-4bf9-ac71-45c812ad1680
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: "?BeginWrite@CThreadBase@@QAEHK@Z, BeginWrite, BeginWrite method [Windows Management Instrumentation], BeginWrite method [Windows Management Instrumentation],CThreadBase interface, CThreadBase interface [Windows Management Instrumentation],BeginWrite method, CThreadBase.BeginWrite, CThreadBase::BeginWrite, thrdbase/CThreadBase::BeginWrite, wmi.cthreadbase_beginwrite"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TS_TEXTCHANGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FrameDynOS.dll
-	FrameDyn.dll
api_name:
-	CThreadBase.BeginWrite
-	?BeginWrite@CThreadBase@@QAEHK@Z
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# CThreadBase::BeginWrite


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/0511cd5b-f791-4821-8d75-23b0635e2266">CThreadBase</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>BeginWrite</b> method provides thread safety by indicating the beginning of a data write operation when the provider is built on the WMI Provider Framework. <a href="https://msdn.microsoft.com/0511cd5b-f791-4821-8d75-23b0635e2266">CThreadBase</a> is called internally.


## -parameters




### -param dwTimeOut






#### - dwTimeout

Timeout for the write data operation. The default is no timeout.


## -returns



This method does not return a value.



