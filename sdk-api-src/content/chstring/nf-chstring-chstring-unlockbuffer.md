---
UID: NF:chstring.CHString.UnlockBuffer
title: CHString::UnlockBuffer (chstring.h)
description: The UnlockBuffer method unlocks the buffer that was previously secured by calling LockBuffer and resets the reference count to 1.
old-location: wmi\chstring_unlockbuffer.htm
tech.root: WmiSdk
ms.assetid: cde732ea-b2de-4eb7-bef6-bed01137d76a
ms.date: 12/05/2018
ms.keywords: CHString interface [Windows Management Instrumentation],UnlockBuffer method, CHString.UnlockBuffer, CHString::UnlockBuffer, UnlockBuffer, UnlockBuffer method [Windows Management Instrumentation], UnlockBuffer method [Windows Management Instrumentation],CHString interface, _hmm_chstring_unlockbuffer, chstring/CHString::UnlockBuffer, wmi.chstring_unlockbuffer
f1_keywords:
- chstring/CHString.UnlockBuffer
dev_langs:
- c++
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
- CHString.UnlockBuffer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CHString::UnlockBuffer


## -description


<p class="CCE_Message">[The <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/chstring">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>UnlockBuffer</b> method unlocks the buffer that was previously secured by calling <a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-lockbuffer">LockBuffer</a> and resets the reference count to 1.


## -parameters






## -returns



This method does not return a value.




## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/chstring">CHString</a> destructor implies <b>UnlockBuffer</b> to ensure that you do not leave the buffer locked when the destructor is called.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/chstring">CHString</a>



<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-lockbuffer">CHString::LockBuffer</a>
 

 

