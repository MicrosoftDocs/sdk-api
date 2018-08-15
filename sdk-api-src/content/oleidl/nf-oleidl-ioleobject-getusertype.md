---
UID: NF:oleidl.IOleObject.GetUserType
title: IOleObject::GetUserType
author: windows-sdk-content
description: Retrieves the user-type name of an object for display in user-interface elements such as menus, list boxes, and dialog boxes.
old-location: com\ioleobject_getusertype.htm
old-project: com
ms.assetid: 8ffffa01-d118-4955-84d1-a4659ba9ddc9
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetUserType, GetUserType method [COM], GetUserType method [COM],IOleObject interface, IOleObject interface [COM],GetUserType method, IOleObject.GetUserType, IOleObject::GetUserType, _ole_ioleobject_getusertype, com.ioleobject_getusertype, oleidl/IOleObject::GetUserType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: oleidl.h
req.include-header: 
req.redist: 
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
 - IOleObject.GetUserType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IOleObject::GetUserType


## -description


Retrieves the user-type name of an object for display in user-interface elements such as menus, list boxes, and dialog boxes.


## -parameters




### -param dwFormOfType [in]

The form of the user-type name to be presented to users. Possible values are obtained from the <a href="https://msdn.microsoft.com/f35dd18a-7fde-4954-8315-bc9bfd933827">USERCLASSTYPE</a> enumeration.


### -param pszUserType [out]

Address of <a href="https://msdn.microsoft.com/730d5e23-e84a-4629-9b59-492d8536122e">LPOLESTR</a> pointer variable that receives a pointer to the user type string. The caller must free <i>pszUserType</i> using the current <a href="https://msdn.microsoft.com/047f281e-2665-4d6d-9a0b-918cd3339447">IMalloc</a> instance. If an error occurs, the implementation must set <i>pszUserType</i> to <b>NULL</b>.


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
<dt><b>OLE_S_USEREG</b></dt>
</dl>
</td>
<td width="60%">
Delegate to the default handler's implementation using the registry to provide the requested information.

</td>
</tr>
</table>
 




## -remarks



Containers call <b>IOleObject::GetUserType</b> in order to represent embedded objects in list boxes, menus, and dialog boxes by their normal, user-recognizable names. Examples include "Word Document," "Excel Chart," and "Paintbrush Object." The information returned by <b>IOleObject::GetUserType</b> is the user-readable equivalent of the binary class identifier returned by <a href="https://msdn.microsoft.com/4b3c0292-0476-4f56-abd2-2f3a82195c67">IOleObject::GetUserClassID</a>.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The default handler's implementation of <b>IOleObject::GetUserType</b> uses the object's class identifier (the <i>pClsid</i> parameter returned by <a href="https://msdn.microsoft.com/4b3c0292-0476-4f56-abd2-2f3a82195c67">IOleObject::GetUserClassID</a>) and the <i>dwFormOfType</i> parameter together as a key into the registry. If an entry is found that matches the key exactly, then the user type specified by that entry is returned. If only the CLSID part of the key matches, then the lowest-numbered entry available (usually the full name) is used. If the CLSID is not found, or there are no user types registered for the class, the user type currently found in the object's storage is used.

You should not cache the string returned from <b>IOleObject::GetUserType</b>. Instead, call this method each and every time the string is needed. This guarantees correct results when the embedded object is being converted from one type into another without the caller's knowledge. Calling this method is inexpensive because the default handler implements it using the registry.


<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
You can use the implementation provided by the default handler by returning OLE_S_USEREG as your application's implementation of this method. If the user type name is an empty string, the message "Unknown Object" is returned.

You can call the OLE helper function <a href="https://msdn.microsoft.com/492a4084-494e-4d78-8f3a-853ec486a2d6">OleRegGetUserType</a> to return the appropriate user type.




## -see-also




<a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>



<a href="https://msdn.microsoft.com/4b3c0292-0476-4f56-abd2-2f3a82195c67">IOleObject::GetUserClassID</a>



<a href="https://msdn.microsoft.com/38cccb3d-e198-4996-991b-6c56451d25e3">IOleObject::SetHostNames</a>



<a href="https://msdn.microsoft.com/492a4084-494e-4d78-8f3a-853ec486a2d6">OleRegGetUserType</a>



<a href="https://msdn.microsoft.com/6f26550d-c094-4150-b8ef-2da1d052c1ff">ReadFmtUserTypeStg</a>



<a href="https://msdn.microsoft.com/f35dd18a-7fde-4954-8315-bc9bfd933827">USERCLASSTYPE</a>
 

 

