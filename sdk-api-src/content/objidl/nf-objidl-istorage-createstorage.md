---
UID: NF:objidl.IStorage.CreateStorage
title: IStorage::CreateStorage (objidl.h)
author: windows-sdk-content
description: Creates and opens a new storage object nested within this storage object with the specified name in the specified access mode.
old-location: stg\istorage_createstorage.htm
tech.root: Stg
ms.assetid: 8c74cacf-8d3c-4d57-b1e9-dc5e4f281717
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateStorage, CreateStorage method [Structured Storage], CreateStorage method [Structured Storage],IStorage interface, IStorage interface [Structured Storage],CreateStorage method, IStorage.CreateStorage, IStorage::CreateStorage, _stg_istorage_createstorage, objidl/IStorage::CreateStorage, stg.istorage_createstorage
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IStorage.CreateStorage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStorage::CreateStorage


## -description


The <b>CreateStorage</b> method
			 creates and opens a new storage object nested within this storage object with the specified name in the specified access mode.


## -parameters




### -param pwcsName [in]

A pointer to a wide character null-terminated Unicode string that contains the name of the newly created storage object. The name can be used later to reopen the storage object. The name must not exceed 31 characters in length, not including the string terminator. The 000 through 01f characters, serving as the first character of the stream/storage name, are reserved for use by OLE. This is a compound file restriction, not a structured storage restriction.


### -param grfMode [in]

A value that specifies the access mode to use when opening the newly created storage object. For more information and a description of possible values, see <a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM Constants</a>.


### -param reserved1 [in]

Reserved for future use; must be zero.


### -param reserved2 [in]

Reserved for future use; must be zero.


### -param ppstg [out]

A pointer, when successful, to the location of the 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> pointer to the newly created storage object. This parameter is set to <b>NULL</b> if an error occurs.


## -returns



This method can return one of these values.




## -remarks



If a storage with the name specified in the <i>pwcsName</i> parameter already exists within the parent storage object, and the <i>grfMode</i> parameter includes the STGM_CREATE flag, the existing storage is replaced by the new one. If the <i>grfMode</i> parameter includes the STGM_CONVERT flag, the existing element is converted to a stream object named CONTENTS and the new storage object is created containing the CONTENTS stream object. The destruction of the old element and the creation of the new storage object are both subject to the transaction mode on the parent storage object. Be aware that you cannot use STGM_CONVERT if you are also using STGM_CREATE.

The COM-provided compound file implementation of the <b>IStorage::CreateStorage</b> method does not support the following behavior:

<ul>
<li>The STGM_PRIORITY flag for nonroot storages.</li>
<li>Opening the same storage object more than once from the same parent storage. The STGM_SHARE_EXCLUSIVE flag must be specified.</li>
<li>The STGM_DELETEONRELEASE flag. If this flag is specified, the function returns STG_E_INVALIDFLAG.</li>
</ul>
If a storage object with the same name already exists and <i>grfMode</i> is set to STGM_FAILIFTHERE, this method fails with the return value STG_E_FILEALREADYEXISTS.




## -see-also




<a href="https://msdn.microsoft.com/2a2253f6-d3d3-403e-a9ba-53a541c7a31e">IStorage - Compound File Implementation</a>



<a href="https://msdn.microsoft.com/f1f0564e-0ecd-4b73-8863-9d6b6746fd02">IStorage::OpenStorage</a>
 

 

