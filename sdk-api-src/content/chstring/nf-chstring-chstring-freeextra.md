---
UID: NF:chstring.CHString.FreeExtra
title: CHString::FreeExtra
author: windows-sdk-content
description: The FreeExtra method frees any extra memory that was previously allocated by the string but is no longer needed.
old-location: wmi\chstring_freeextra.htm
old-project: WmiSdk
ms.assetid: 4330564e-aeae-4ff3-b01d-eceace721c14
ms.author: windowssdkdev
ms.date: 04/11/2018
ms.keywords: CHString interface [Windows Management Instrumentation],FreeExtra method, CHString.FreeExtra, CHString::FreeExtra, FreeExtra, FreeExtra method [Windows Management Instrumentation], FreeExtra method [Windows Management Instrumentation],CHString interface, _hmm_chstring_freeextra, chstring/CHString::FreeExtra, wmi.chstring_freeextra
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: chstring.h
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
req.typenames: CONFLICT_DETAILS_W, *PCONFLICT_DETAILS_W
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FrameDynOS.dll
-	FrameDyn.dll
api_name:
-	CHString.FreeExtra
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
---

# CHString::FreeExtra


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>FreeExtra</b> method frees any extra memory that was previously allocated by the string but is no longer needed. This method, which reallocates the buffer to the exact length returned by <a href="https://msdn.microsoft.com/b898f9d1-b9a2-4c7b-a7c0-1b6b51ae565f">GetLength</a>, should reduce the memory overhead consumed by the string object.


## -parameters






## -returns



This method does not return a value.



