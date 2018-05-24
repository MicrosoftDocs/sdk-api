---
UID: NF:oleidl.IOleObject.Unadvise
title: IOleObject::Unadvise
author: windows-driver-content
description: Deletes a previously established advisory connection.
old-location: com\ioleobject_unadvise.htm
old-project: com
ms.assetid: e3d63a75-30b0-4fe5-9a1d-c70820583765
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IOleObject interface [COM],Unadvise method, IOleObject.Unadvise, IOleObject::Unadvise, Unadvise, Unadvise method [COM], Unadvise method [COM],IOleObject interface, _ole_ioleobject_unadvise, com.ioleobject_unadvise, oleidl/IOleObject::Unadvise
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: USERCLASSTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OleIdl.h
api_name:
-	IOleObject.Unadvise
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

