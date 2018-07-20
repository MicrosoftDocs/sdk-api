---
UID: NF:objidl.IStorage.MoveElementTo
title: IStorage::MoveElementTo
author: windows-sdk-content
description: The MoveElementTo method copies or moves a substorage or stream from this storage object to another storage object.
old-location: stg\istorage_moveelementto.htm
old-project: stg
ms.assetid: d9d33c64-edac-480f-b295-b2a06e51af2e
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: IStorage interface [Structured Storage],MoveElementTo method, IStorage.MoveElementTo, IStorage::MoveElementTo, MoveElementTo, MoveElementTo method [Structured Storage], MoveElementTo method [Structured Storage],IStorage interface, _stg_istorage_moveelementto, objidl/IStorage::MoveElementTo, stg.istorage_moveelementto
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IStorage.MoveElementTo
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# IStorage::MoveElementTo


## -description


The <b>MoveElementTo</b> method copies or moves a substorage or stream from this storage object to another storage object.


## -parameters




### -param pwcsName [in]

Pointer to a wide character null-terminated Unicode string that contains the name of the element in this storage object to be moved or copied.


### -param pstgDest [in]


<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> pointer to the destination storage object.


### -param pwcsNewName [in]

Pointer to a wide character null-terminated unicode string that contains the new name for the element in its new storage object.


### -param grfFlags [in]

Specifies whether the operation should be a move (STGMOVE_MOVE) or a copy (STGMOVE_COPY). See the 
<a href="https://msdn.microsoft.com/f55c376b-f150-406a-b960-f096c2deeff1">STGMOVE</a> enumeration.


## -returns



This method can return one of these values.




## -remarks



The <b>IStorage::MoveElementTo</b> method is typically the same as invoking the 
<a href="https://msdn.microsoft.com/8b25b32b-f739-406a-96e8-dba687c7f055">IStorage::CopyTo</a> method on the indicated element and then removing the source element. In this case, the 
<b>MoveElementTo</b> method uses only the publicly available functions of the destination storage object to carry out the move.

If the source and destination storage objects have special knowledge about each other's implementation (they could, for example, be different instances of the same implementation), this method can be implemented more efficiently.

Before calling this method, the element to be moved must be closed, and the destination storage must be open. Also, the destination object and element cannot be the same storage object/element name as the source of the move. That is, you cannot move an element to itself.




## -see-also




<a href="https://msdn.microsoft.com/2a2253f6-d3d3-403e-a9ba-53a541c7a31e">IStorage - Compound File Implementation</a>



<a href="https://msdn.microsoft.com/8b25b32b-f739-406a-96e8-dba687c7f055">IStorage::CopyTo</a>



<a href="https://msdn.microsoft.com/f55c376b-f150-406a-b960-f096c2deeff1">STGMOVE</a>
 

 

