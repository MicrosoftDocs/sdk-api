---
UID: NF:chstring.CHString.LockBuffer
title: CHString::LockBuffer (chstring.h)
description: The LockBuffer method locks a string in the buffer.
helpviewer_keywords: ["CHString interface [Windows Management Instrumentation]","LockBuffer method","CHString.LockBuffer","CHString::LockBuffer","LockBuffer","LockBuffer method [Windows Management Instrumentation]","LockBuffer method [Windows Management Instrumentation]","CHString interface","_hmm_chstring_lockbuffer","chstring/CHString::LockBuffer","wmi.chstring_lockbuffer"]
old-location: wmi\chstring_lockbuffer.htm
tech.root: wmi
ms.assetid: 820a3ff5-4f99-40b0-8a9d-e5c22fea7ddb
ms.date: 12/05/2018
ms.keywords: CHString interface [Windows Management Instrumentation],LockBuffer method, CHString.LockBuffer, CHString::LockBuffer, LockBuffer, LockBuffer method [Windows Management Instrumentation], LockBuffer method [Windows Management Instrumentation],CHString interface, _hmm_chstring_lockbuffer, chstring/CHString::LockBuffer, wmi.chstring_lockbuffer
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
 - CHString::LockBuffer
 - chstring/CHString::LockBuffer
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
 - CHString.LockBuffer
---

# CHString::LockBuffer


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/chstring">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>LockBuffer</b> method locks a string in the buffer.



## -returns

Returns a pointer to a <a href="/windows/desktop/WmiSdk/chstring">CHString</a> object or a <b>NULL</b>-terminated string.

## -remarks

By calling <b>LockBuffer</b>, you create a copy of the string and then set the reference count to -1.

When the reference count is set to -1, the string in the buffer is considered to be in a locked state, which protects the string in the following two ways:

<ul>
<li>No other string can get a reference to the data in the locked string, even if that string is assigned to the locked string.</li>
<li>The locked string never references another string, even if that other string is copied to the locked string.</li>
</ul>
By locking the string in the buffer, you ensure that the string's exclusive hold on the buffer remains intact.

After you have finished with <b>LockBuffer</b>, call <a href="/windows/desktop/api/chstring/nf-chstring-chstring-unlockbuffer">UnlockBuffer</a> to reset the reference count to 1 (one).

## -see-also

<a href="/windows/desktop/WmiSdk/chstring">CHString</a>



<a href="/windows/desktop/api/chstring/nf-chstring-chstring-unlockbuffer">CHString::UnlockBuffer</a>
