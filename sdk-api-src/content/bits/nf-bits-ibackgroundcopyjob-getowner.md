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

# IBackgroundCopyJob::GetOwner


## -description


Retrieves the identity of the job's owner.


## -parameters




### -param pVal






#### - ppOwner [out]

Null-terminated string that contains the string version of the SID that identifies the job's owner. Call the 
<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function to free <i>ppOwner</i> when done.


## -returns



This method returns the following <b>HRESULT</b> values, as well as others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
Job owner's identity was successfully retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppOwner</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



To convert the string format of the SID into a domain\user-name format, which is suitable for display in a user interface, call the following functions:

<ul>
<li>To convert the string SID to a SID, call the 
<a href="https://msdn.microsoft.com/bf7262e3-ad2c-44c4-99cb-dcf29ad36efd">ConvertStringSidToSid</a> function.</li>
<li>To retrieve the domain and user name associated with the SID, call the 
<a href="https://msdn.microsoft.com/b8a44ffc-86e1-4f79-ad51-8340da9eaefd">LookupAccountSid</a> function.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/12ac2dd8-516b-4b5d-a2bf-0abb55d18ee0">IBackgroundCopyJob::TakeOwnership</a>
 

 

