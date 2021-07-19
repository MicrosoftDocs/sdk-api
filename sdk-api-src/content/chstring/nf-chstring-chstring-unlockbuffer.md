---
UID: NF:chstring.CHString.UnlockBuffer
title: CHString::UnlockBuffer (chstring.h)
description: The UnlockBuffer method unlocks the buffer that was previously secured by calling LockBuffer and resets the reference count to 1.
helpviewer_keywords: ["CHString interface [Windows Management Instrumentation]","UnlockBuffer method","CHString.UnlockBuffer","CHString::UnlockBuffer","UnlockBuffer","UnlockBuffer method [Windows Management Instrumentation]","UnlockBuffer method [Windows Management Instrumentation]","CHString interface","_hmm_chstring_unlockbuffer","chstring/CHString::UnlockBuffer","wmi.chstring_unlockbuffer"]
old-location: wmi\chstring_unlockbuffer.htm
tech.root: wmi
ms.assetid: cde732ea-b2de-4eb7-bef6-bed01137d76a
ms.date: 12/05/2018
ms.keywords: CHString interface [Windows Management Instrumentation],UnlockBuffer method, CHString.UnlockBuffer, CHString::UnlockBuffer, UnlockBuffer, UnlockBuffer method [Windows Management Instrumentation], UnlockBuffer method [Windows Management Instrumentation],CHString interface, _hmm_chstring_unlockbuffer, chstring/CHString::UnlockBuffer, wmi.chstring_unlockbuffer
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CHString::UnlockBuffer
 - chstring/CHString::UnlockBuffer
dev_langs:
 - c++
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
---

# CHString::UnlockBuffer


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/chstring">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>UnlockBuffer</b> method unlocks the buffer that was previously secured by calling <a href="/windows/desktop/api/chstring/nf-chstring-chstring-lockbuffer">LockBuffer</a> and resets the reference count to 1.



## -remarks

The <a href="/windows/desktop/WmiSdk/chstring">CHString</a> destructor implies <b>UnlockBuffer</b> to ensure that you do not leave the buffer locked when the destructor is called.

## -see-also

<a href="/windows/desktop/WmiSdk/chstring">CHString</a>



<a href="/windows/desktop/api/chstring/nf-chstring-chstring-lockbuffer">CHString::LockBuffer</a>
