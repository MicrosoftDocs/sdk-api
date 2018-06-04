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

# CHString::ReleaseBuffer


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>ReleaseBuffer</b> method ends the use of a buffer allocated by <a href="https://msdn.microsoft.com/library/windows/hardware/jj983413">GetBuffer</a>.


## -parameters




### -param nNewLength

The new length of the string in characters, not counting a terminating <b>null</b> character.

If the string is <b>NULL</b>-terminated, the –1 default value sets the <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> string size to the current length of the string.


## -returns



This method does not return a value.




## -remarks



If you know that the string in the buffer is <b>NULL</b>-terminated, you can omit the <i>nNewLength</i> parameter. If your string is not <b>NULL</b>-terminated, then use <i>nNewLength</i> to specify its length. The address returned by <a href="https://msdn.microsoft.com/library/windows/hardware/jj983413">GetBuffer</a> is not valid after the call to <b>ReleaseBuffer</b> or any other <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> operation.




## -see-also




<a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a>



<a href="https://msdn.microsoft.com/07fa7cae-8af6-491b-a561-8947afde47ab">CHString::GetBuffer</a>
 

 

