---
UID: NF:chstring.CHString.GetBuffer
title: CHString::GetBuffer (chstring.h)
description: The GetBuffer method returns a pointer to the internal character buffer for the CHString object.
helpviewer_keywords: ["?GetBuffer@CHString@@QAEPAGH@Z","?GetBuffer@CHString@@QEAAPEAGH@Z","CHString interface [Windows Management Instrumentation]","GetBuffer method","CHString.GetBuffer","CHString::GetBuffer","GetBuffer","GetBuffer method [Windows Management Instrumentation]","GetBuffer method [Windows Management Instrumentation]","CHString interface","_hmm_chstring_getbuffer","chstring/CHString::GetBuffer","wmi.chstring_getbuffer"]
old-location: wmi\chstring_getbuffer.htm
tech.root: wmi
ms.assetid: 07fa7cae-8af6-491b-a561-8947afde47ab
ms.date: 12/05/2018
ms.keywords: ?GetBuffer@CHString@@QAEPAGH@Z, ?GetBuffer@CHString@@QEAAPEAGH@Z, CHString interface [Windows Management Instrumentation],GetBuffer method, CHString.GetBuffer, CHString::GetBuffer, GetBuffer, GetBuffer method [Windows Management Instrumentation], GetBuffer method [Windows Management Instrumentation],CHString interface, _hmm_chstring_getbuffer, chstring/CHString::GetBuffer, wmi.chstring_getbuffer
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
 - CHString::GetBuffer
 - chstring/CHString::GetBuffer
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
 - CHString.GetBuffer
 - ?GetBuffer@CHString@@QAEPAGH@Z
 - ?GetBuffer@CHString@@QEAAPEAGH@Z
---

# CHString::GetBuffer


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/chstring">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetBuffer</b> method returns a pointer to the internal character buffer for the <a href="/windows/desktop/WmiSdk/chstring">CHString</a> object.

## -parameters

### -param nMinBufLength

The minimum size of the character buffer in characters. This value does not include space for a <b>NULL</b> terminator.

## -returns

An <b>LPWSTR</b> pointer to the object's (<b>NULL</b>-terminated) character buffer.

## -remarks

The returned <b>LPWSTR</b> is not <b>const</b> and therefore allows direct modification of <a href="/windows/desktop/WmiSdk/chstring">CHString</a> contents.

If you use the pointer returned by <b>GetBuffer</b> to change the string contents, you must call <a href="/windows/desktop/api/chstring/nf-chstring-chstring-releasebuffer">ReleaseBuffer</a> before using any other <a href="/windows/desktop/WmiSdk/chstring">CHString</a> methods.

After a call to <a href="/windows/desktop/api/chstring/nf-chstring-chstring-releasebuffer">ReleaseBuffer</a>, the address returned by <b>GetBuffer</b> may not be valid because additional <a href="/windows/desktop/WmiSdk/chstring">CHString</a> operations can cause the <b>CHString</b> buffer to be reallocated. If you do not change the length of the <b>CHString</b> string, the buffer is not reallocated. The buffer memory is freed automatically when the <b>CHString</b> object is destroyed.

Note that if you keep track of the string length yourself, you should not append the terminating <b>NULL</b> character. You must, however, specify the final string length when you release the buffer with <a href="/windows/desktop/api/chstring/nf-chstring-chstring-releasebuffer">ReleaseBuffer</a>. If you do append a terminating <b>NULL</b> character, you should pass –1 for the length to <b>ReleaseBuffer</b>, which calls <b>wcslen</b> on the buffer to determine its length.

## -see-also

<a href="/windows/desktop/WmiSdk/chstring">CHString</a>



<a href="/windows/desktop/api/chstring/nf-chstring-chstring-getbuffersetlength">CHString::GetBufferSetLength</a>



<a href="/windows/desktop/api/chstring/nf-chstring-chstring-releasebuffer">CHString::ReleaseBuffer</a>