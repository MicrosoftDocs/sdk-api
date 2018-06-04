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

# IOleObject::Unadvise


## -description


Deletes a previously established advisory connection.


## -parameters




### -param dwConnection [in]

Contains a token of nonzero value, which was previously returned from <a href="https://msdn.microsoft.com/6a68c9e9-6e06-4def-89a5-18e184e76a26">IOleObject::Advise</a> through its <i>pdwConnection</i> parameter.


## -returns



This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The operation failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_NOCONNECTION</b></dt>
</dl>
</td>
<td width="60%">
dwConnection does not represent a valid advisory connection.

</td>
</tr>
</table>
 




## -remarks



Normally, containers call <b>IOleObject::Unadvise</b> at shutdown or when an object is deleted. In certain cases, containers can call this method on objects that are running but not currently visible as a way of reducing the overhead of maintaining multiple advisory connections. The easiest way to implement this method is to delegate the call to <b>IOleObject::Unadvise</b>.




## -see-also




<a href="https://msdn.microsoft.com/620bc43f-dfc7-48b7-a574-ca7287ffa42f">IOleAdviseHolder::Unadvise</a>



<a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>



<a href="https://msdn.microsoft.com/6a68c9e9-6e06-4def-89a5-18e184e76a26">IOleObject::Advise</a>



<a href="https://msdn.microsoft.com/4e1d6d9e-ebf2-4cd6-b7b4-00f9e7bd9bdc">IOleObject::EnumAdvise</a>
 

 

