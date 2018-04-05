---
UID: NF:thrdbase.CThreadBase.OnFinalRelease
title: CThreadBase::OnFinalRelease method
author: windows-driver-content
description: The OnFinalRelease method is a virtual function called by Release when the reference count reaches zero. CThreadBase is called internally.
old-location: wmi\cthreadbase_onfinalrelease.htm
old-project: WmiSdk
ms.assetid: a17a379d-60ba-4a76-8900-58fabadad5ea
ms.author: windowsdriverdev
ms.date: 3/16/2018
ms.keywords: "?OnFinalRelease@CThreadBase@@MAEXXZ, ?OnFinalRelease@CThreadBase@@MEAAXXZ, CThreadBase, CThreadBase interface [Windows Management Instrumentation], OnFinalRelease method, CThreadBase::OnFinalRelease, OnFinalRelease method [Windows Management Instrumentation], OnFinalRelease method [Windows Management Instrumentation], CThreadBase interface, OnFinalRelease,CThreadBase.OnFinalRelease, thrdbase/CThreadBase::OnFinalRelease, wmi.cthreadbase_onfinalrelease"
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	CThreadBase.OnFinalRelease
-	?OnFinalRelease@CThreadBase@@MAEXXZ
-	?OnFinalRelease@CThreadBase@@MEAAXXZ
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# CThreadBase::OnFinalRelease method


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/0511cd5b-f791-4821-8d75-23b0635e2266">CThreadBase</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>OnFinalRelease</b>  method  is a virtual function called by <a href="_com_iunknown_release">Release</a> when the reference count reaches zero. <a href="https://msdn.microsoft.com/0511cd5b-f791-4821-8d75-23b0635e2266">CThreadBase</a> is called internally.


## -parameters






## -returns



This method does not return a value.



