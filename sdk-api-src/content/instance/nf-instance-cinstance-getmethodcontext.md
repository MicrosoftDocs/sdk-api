---
UID: NF:instance.CInstance.GetMethodContext
title: CInstance::GetMethodContext
author: windows-sdk-content
description: The GetMethodContext method returns a pointer to a MethodContext object.
old-location: wmi\cinstance_getmethodcontext.htm
tech.root: WmiSdk
ms.assetid: a2033754-4fd0-405f-9ad9-737eb8931016
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "?GetMethodContext@CInstance@@QBEPAVMethodContext@@XZ, ?GetMethodContext@CInstance@@QEBAPEAVMethodContext@@XZ, CInstance interface [Windows Management Instrumentation],GetMethodContext method, CInstance.GetMethodContext, CInstance::GetMethodContext, GetMethodContext, GetMethodContext method [Windows Management Instrumentation], GetMethodContext method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_getmethodcontext, instance/CInstance::GetMethodContext, wmi.cinstance_getmethodcontext"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CInstance.GetMethodContext
 - ?GetMethodContext@CInstance@@QBEPAVMethodContext@@XZ
 - ?GetMethodContext@CInstance@@QEBAPEAVMethodContext@@XZ
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- instance.h
: 
- CInstance.GetMethodContext
: 
---

# CInstance::GetMethodContext


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetMethodContext</b> method returns a pointer to a <b>MethodContext</b> object.


## -parameters






## -returns



Returns a pointer to the current <b>MethodContext</b> object.




## -remarks



Framework providers should not release the <b>MethodContext</b> pointer returned by this function.



