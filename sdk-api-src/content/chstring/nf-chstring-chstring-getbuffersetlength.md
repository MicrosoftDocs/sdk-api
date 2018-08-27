---
UID: NF:chstring.CHString.GetBufferSetLength
title: CHString::GetBufferSetLength
author: windows-sdk-content
description: The GetBufferSetLength method returns a pointer to the internal character buffer for the CHString object, truncating or increasing its length if necessary to exactly match the length specified in nNewLength.
old-location: wmi\chstring_getbuffersetlength.htm
old-project: WmiSdk
ms.assetid: de40f3a3-1880-426d-b3c2-864f0f45f218
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: CHString interface [Windows Management Instrumentation],GetBufferSetLength method, CHString.GetBufferSetLength, CHString::GetBufferSetLength, GetBufferSetLength, GetBufferSetLength method [Windows Management Instrumentation], GetBufferSetLength method [Windows Management Instrumentation],CHString interface, _hmm_chstring_getbuffersetlength, chstring/CHString::GetBufferSetLength, wmi.chstring_getbuffersetlength
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: chstring.h
req.include-header: FwCommon.h
req.redist: 
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
req.typenames: CONFLICT_DETAILS_W, *PCONFLICT_DETAILS_W
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
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
---

# CHString::GetBufferSetLength


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetBufferSetLength</b> method returns a pointer to the internal character buffer for the <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> object, truncating or increasing its length if necessary to exactly match the length specified in <i>nNewLength</i>.


## -parameters




### -param nNewLength

Exact size of the <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> character buffer, measured in characters.


## -returns



Returns an <b>LPWSTR</b> pointer to the object's (NULL-terminated) character buffer.




## -remarks



The returned <b>LPWSTR</b> pointer, which is not <b>const</b>, allows direct modification of <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> contents.

If you use the pointer returned by <a href="https://msdn.microsoft.com/07fa7cae-8af6-491b-a561-8947afde47ab">GetBuffer</a> to change the string contents, you must call <a href="https://msdn.microsoft.com/55de2960-8a71-48cc-862b-7cf9a4edf8ea">ReleaseBuffer</a> before using any other <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> methods.

After a call to <a href="https://msdn.microsoft.com/55de2960-8a71-48cc-862b-7cf9a4edf8ea">ReleaseBuffer</a>, the address returned by <b>GetBufferSetLength</b> may not be valid because additional <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> operations can cause the <b>CHString</b> buffer to be reallocated. If you do not change the length of the <b>CHString</b> string, the buffer is not reassigned. The buffer memory is freed automatically when the <b>CHString</b> object is destroyed.

Note that if you keep track of the string length yourself, you should not append the terminating <b>NULL</b> character. You must, however, specify the final string length when you release the buffer with <a href="https://msdn.microsoft.com/55de2960-8a71-48cc-862b-7cf9a4edf8ea">ReleaseBuffer</a>. If you do append a terminating <b>NULL</b> character when you call <b>ReleaseBuffer</b>, you should pass –1 (the default) for the length. The <b>ReleaseBuffer</b> method calls the wcslen function on the buffer to determine its length.


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




<a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a>



<a href="https://msdn.microsoft.com/07fa7cae-8af6-491b-a561-8947afde47ab">CHString::GetBuffer</a>



<a href="https://msdn.microsoft.com/55de2960-8a71-48cc-862b-7cf9a4edf8ea">CHString::ReleaseBuffer</a>
 

 

