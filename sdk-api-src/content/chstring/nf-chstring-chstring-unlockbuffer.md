---
UID: NF:chstring.CHString.UnlockBuffer
title: CHString::UnlockBuffer
author: windows-driver-content
description: The UnlockBuffer method unlocks the buffer that was previously secured by calling LockBuffer and resets the reference count to 1.
old-location: wmi\chstring_unlockbuffer.htm
old-project: WmiSdk
ms.assetid: cde732ea-b2de-4eb7-bef6-bed01137d76a
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: CHString interface [Windows Management Instrumentation],UnlockBuffer method, CHString.UnlockBuffer, CHString::UnlockBuffer, UnlockBuffer, UnlockBuffer method [Windows Management Instrumentation], UnlockBuffer method [Windows Management Instrumentation],CHString interface, _hmm_chstring_unlockbuffer, chstring/CHString::UnlockBuffer, wmi.chstring_unlockbuffer
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: CF_SYNC_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FrameDynOS.dll
-	FrameDyn.dll
api_name:
-	CHString.UnlockBuffer
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
---

# CHString::UnlockBuffer


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>UnlockBuffer</b> method unlocks the buffer that was previously secured by calling <a href="https://msdn.microsoft.com/820a3ff5-4f99-40b0-8a9d-e5c22fea7ddb">LockBuffer</a> and resets the reference count to 1.


## -parameters






## -returns



This method does not return a value.




## -remarks



The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> destructor implies <b>UnlockBuffer</b> to ensure that you do not leave the buffer locked when the destructor is called.




## -see-also




<a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a>



<a href="https://msdn.microsoft.com/820a3ff5-4f99-40b0-8a9d-e5c22fea7ddb">CHString::LockBuffer</a>
 

 

