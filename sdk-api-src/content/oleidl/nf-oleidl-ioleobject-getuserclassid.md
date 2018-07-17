---
UID: NF:oleidl.IOleObject.GetUserClassID
title: IOleObject::GetUserClassID
author: windows-sdk-content
description: Retrieves an object's class identifier, the CLSID corresponding to the string identifying the object to an end user.
old-location: com\ioleobject_getuserclassid.htm
old-project: com
ms.assetid: 4b3c0292-0476-4f56-abd2-2f3a82195c67
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetUserClassID, GetUserClassID method [COM], GetUserClassID method [COM],IOleObject interface, IOleObject interface [COM],GetUserClassID method, IOleObject.GetUserClassID, IOleObject::GetUserClassID, _ole_ioleobject_getuserclassid, com.ioleobject_getuserclassid, oleidl/IOleObject::GetUserClassID
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: USERCLASSTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleObject.GetUserClassID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IOleObject::GetUserClassID


## -description


Retrieves an object's class identifier, the CLSID corresponding to the string identifying the object to an end user.


## -parameters




### -param pClsid [out]

Pointer to the class identifier (CLSID) to be returned. An object's CLSID is the binary equivalent of the user-type name returned by <a href="https://msdn.microsoft.com/8ffffa01-d118-4955-84d1-a4659ba9ddc9">IOleObject::GetUserType</a>.


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
</table>
 




## -remarks



<b>IOleObject::GetUserClassID</b> returns the CLSID associated with the object in the registration database. Normally, this value is identical to the CLSID stored with the object, which is returned by <a href="https://msdn.microsoft.com/921a3b86-a240-454e-9411-8d653e02b90e">IPersist::GetClassID</a>. For linked objects, this is the CLSID of the last bound link source. If the object is running in an application different from the one in which it was created and for the purpose of being edited is emulating a class that the container application recognizes, the CLSID returned will be that of the class being emulated rather than that of the object's own class.




## -see-also




<a href="https://msdn.microsoft.com/748649a2-cf75-4ffa-ac1f-4a148b845d21">GetConvertStg</a>



<a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>



<a href="https://msdn.microsoft.com/8ffffa01-d118-4955-84d1-a4659ba9ddc9">IOleObject::GetUserType</a>



<a href="https://msdn.microsoft.com/921a3b86-a240-454e-9411-8d653e02b90e">IPersist::GetClassID</a>



<a href="https://msdn.microsoft.com/fe470f8a-b2f0-48a4-a270-77420bd1472a">OleDoAutoConvert</a>



<a href="https://msdn.microsoft.com/39abf385-962a-4b20-b319-501c8130e050">OleSetAutoConvert</a>



<a href="https://msdn.microsoft.com/98c8fd20-6384-4656-941c-1f24d9a4d4a9">SetConvertStg</a>
 

 

