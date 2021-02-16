---
UID: NF:chstring.CHString.GetBufferSetLength
title: CHString::GetBufferSetLength (chstring.h)
description: The GetBufferSetLength method returns a pointer to the internal character buffer for the CHString object, truncating or increasing its length if necessary to exactly match the length specified in nNewLength.
helpviewer_keywords: ["CHString interface [Windows Management Instrumentation]","GetBufferSetLength method","CHString.GetBufferSetLength","CHString::GetBufferSetLength","GetBufferSetLength","GetBufferSetLength method [Windows Management Instrumentation]","GetBufferSetLength method [Windows Management Instrumentation]","CHString interface","_hmm_chstring_getbuffersetlength","chstring/CHString::GetBufferSetLength","wmi.chstring_getbuffersetlength"]
old-location: wmi\chstring_getbuffersetlength.htm
tech.root: wmi
ms.assetid: de40f3a3-1880-426d-b3c2-864f0f45f218
ms.date: 12/05/2018
ms.keywords: CHString interface [Windows Management Instrumentation],GetBufferSetLength method, CHString.GetBufferSetLength, CHString::GetBufferSetLength, GetBufferSetLength, GetBufferSetLength method [Windows Management Instrumentation], GetBufferSetLength method [Windows Management Instrumentation],CHString interface, _hmm_chstring_getbuffersetlength, chstring/CHString::GetBufferSetLength, wmi.chstring_getbuffersetlength
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
 - CHString::GetBufferSetLength
 - chstring/CHString::GetBufferSetLength
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
 - CHString.GetBufferSetLength
---

# CHString::GetBufferSetLength


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/chstring">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetBufferSetLength</b> method returns a pointer to the internal character buffer for the <a href="/windows/desktop/WmiSdk/chstring">CHString</a> object, truncating or increasing its length if necessary to exactly match the length specified in <i>nNewLength</i>.

## -parameters

### -param nNewLength

Exact size of the <a href="/windows/desktop/WmiSdk/chstring">CHString</a> character buffer, measured in characters.

## -returns

Returns an <b>LPWSTR</b> pointer to the object's (NULL-terminated) character buffer.

## -remarks

The returned <b>LPWSTR</b> pointer, which is not <b>const</b>, allows direct modification of <a href="/windows/desktop/WmiSdk/chstring">CHString</a> contents.

If you use the pointer returned by <a href="/windows/desktop/api/chstring/nf-chstring-chstring-getbuffer">GetBuffer</a> to change the string contents, you must call <a href="/windows/desktop/api/chstring/nf-chstring-chstring-releasebuffer">ReleaseBuffer</a> before using any other <a href="/windows/desktop/WmiSdk/chstring">CHString</a> methods.

After a call to <a href="/windows/desktop/api/chstring/nf-chstring-chstring-releasebuffer">ReleaseBuffer</a>, the address returned by <b>GetBufferSetLength</b> may not be valid because additional <a href="/windows/desktop/WmiSdk/chstring">CHString</a> operations can cause the <b>CHString</b> buffer to be reallocated. If you do not change the length of the <b>CHString</b> string, the buffer is not reassigned. The buffer memory is freed automatically when the <b>CHString</b> object is destroyed.

Note that if you keep track of the string length yourself, you should not append the terminating <b>NULL</b> character. You must, however, specify the final string length when you release the buffer with <a href="/windows/desktop/api/chstring/nf-chstring-chstring-releasebuffer">ReleaseBuffer</a>. If you do append a terminating <b>NULL</b> character when you call <b>ReleaseBuffer</b>, you should pass –1 (the default) for the length. The <b>ReleaseBuffer</b> method calls the wcslen function on the buffer to determine its length.


#### Examples

The following code example shows the use of <b>CHString::GetBufferSetLength</b>.


```cpp
CHString str;
LPWSTR pstr = str.GetBufferSetLength(3);
pstr[0] = 'I';
pstr[1] = 'c';
pstr[2] = 'e';

// No need for trailing zero or call to ReleaseBuffer()
// because GetBufferSetLength() set it for you.

str += " hockey is best!";
printf( "str: %S\n", (LPCWSTR)str );
```

## -see-also

<a href="/windows/desktop/WmiSdk/chstring">CHString</a>



<a href="/windows/desktop/api/chstring/nf-chstring-chstring-getbuffer">CHString::GetBuffer</a>



<a href="/windows/desktop/api/chstring/nf-chstring-chstring-releasebuffer">CHString::ReleaseBuffer</a>