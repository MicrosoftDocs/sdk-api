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

# WriteFmtUserTypeStg function


## -description


The <b>WriteFmtUserTypeStg</b> function writes a clipboard format and user type to the storage object.


## -parameters




### -param pstg

TBD


### -param cf [in]

Specifies the clipboard format that describes the structure of the native area of the storage object. The format tag includes the policy for the names of streams and substorages within this storage object and the rules for interpreting data within those streams.


### -param lpszUserType [in]

Pointer to a null-terminated Unicode string that specifies the object's current user type. The user type value, itself, cannot be <b>NULL</b>. This is the type returned by the 
<a href="_ole_ioleobject_getusertype">IOleObject::GetUserType</a> method. If this function is transported to a remote machine where the object class does not exist, this persistently stored user type can be shown to the user in dialog boxes.


#### - pStg [in]


<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> pointer to the storage object where the information is to be written.


## -returns



This function returns HRESULT.




## -remarks



The 
<b>WriteFmtUserTypeStg</b> function must be called in an object's implementation of the 
<a href="_com_ipersiststorage_save">IPersistStorage::Save</a> method. It must also be called by document-level objects that use structured storage for their persistent representation in their save sequence.

To read the information saved, applications call the 
<a href="https://msdn.microsoft.com/6f26550d-c094-4150-b8ef-2da1d052c1ff">ReadFmtUserTypeStg</a> function.




## -see-also




<a href="_com_ipersiststorage_save">IPersistStorage::Save</a>



<a href="https://msdn.microsoft.com/6f26550d-c094-4150-b8ef-2da1d052c1ff">ReadFmtUserTypeStg</a>
 

 

