---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# CHString::GetBuffer


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetBuffer</b> method returns a pointer to the internal character buffer for the <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> object.


## -parameters




### -param nMinBufLength

The minimum size of the character buffer in characters. This value does not include space for a <b>NULL</b> terminator.


## -returns



An <b>LPWSTR</b> pointer to the object's (<b>NULL</b>-terminated) character buffer.




## -remarks



The returned <b>LPWSTR</b> is not <b>const</b> and therefore allows direct modification of <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> contents.

If you use the pointer returned by <b>GetBuffer</b> to change the string contents, you must call <a href="https://msdn.microsoft.com/55de2960-8a71-48cc-862b-7cf9a4edf8ea">ReleaseBuffer</a> before using any other <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> methods.

After a call to <a href="https://msdn.microsoft.com/55de2960-8a71-48cc-862b-7cf9a4edf8ea">ReleaseBuffer</a>, the address returned by <b>GetBuffer</b> may not be valid because additional <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> operations can cause the <b>CHString</b> buffer to be reallocated. If you do not change the length of the <b>CHString</b> string, the buffer is not reallocated. The buffer memory is freed automatically when the <b>CHString</b> object is destroyed.

Note that if you keep track of the string length yourself, you should not append the terminating <b>NULL</b> character. You must, however, specify the final string length when you release the buffer with <a href="https://msdn.microsoft.com/55de2960-8a71-48cc-862b-7cf9a4edf8ea">ReleaseBuffer</a>. If you do append a terminating <b>NULL</b> character, you should pass –1 for the length to <b>ReleaseBuffer</b>, which calls <b>wcslen</b> on the buffer to determine its length.




## -see-also




<a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a>



<a href="https://msdn.microsoft.com/de40f3a3-1880-426d-b3c2-864f0f45f218">CHString::GetBufferSetLength</a>



<a href="https://msdn.microsoft.com/55de2960-8a71-48cc-862b-7cf9a4edf8ea">CHString::ReleaseBuffer</a>
 

 

