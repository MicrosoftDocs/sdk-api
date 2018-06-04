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

# CHString::LockBuffer


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>LockBuffer</b> method locks a string in the buffer.


## -parameters






## -returns



Returns a pointer to a <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> object or a <b>NULL</b>-terminated string.




## -remarks



By calling <b>LockBuffer</b>, you create a copy of the string and then set the reference count to -1.

When the reference count is set to -1, the string in the buffer is considered to be in a locked state, which protects the string in the following two ways:

<ul>
<li>No other string can get a reference to the data in the locked string, even if that string is assigned to the locked string.</li>
<li>The locked string never references another string, even if that other string is copied to the locked string.</li>
</ul>
By locking the string in the buffer, you ensure that the string's exclusive hold on the buffer remains intact.

After you have finished with <b>LockBuffer</b>, call <a href="https://msdn.microsoft.com/cde732ea-b2de-4eb7-bef6-bed01137d76a">UnlockBuffer</a> to reset the reference count to 1 (one).




## -see-also




<a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a>



<a href="https://msdn.microsoft.com/cde732ea-b2de-4eb7-bef6-bed01137d76a">CHString::UnlockBuffer</a>
 

 

