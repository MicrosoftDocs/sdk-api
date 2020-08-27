---
UID: NF:objidl.IStorage.MoveElementTo
title: IStorage::MoveElementTo (objidl.h)
description: The MoveElementTo method copies or moves a substorage or stream from this storage object to another storage object.
helpviewer_keywords: ["IStorage interface [Structured Storage]","MoveElementTo method","IStorage.MoveElementTo","IStorage::MoveElementTo","MoveElementTo","MoveElementTo method [Structured Storage]","MoveElementTo method [Structured Storage]","IStorage interface","_stg_istorage_moveelementto","objidl/IStorage::MoveElementTo","stg.istorage_moveelementto"]
old-location: stg\istorage_moveelementto.htm
tech.root: Stg
ms.assetid: d9d33c64-edac-480f-b295-b2a06e51af2e
ms.date: 12/05/2018
ms.keywords: IStorage interface [Structured Storage],MoveElementTo method, IStorage.MoveElementTo, IStorage::MoveElementTo, MoveElementTo, MoveElementTo method [Structured Storage], MoveElementTo method [Structured Storage],IStorage interface, _stg_istorage_moveelementto, objidl/IStorage::MoveElementTo, stg.istorage_moveelementto
f1_keywords:
- objidl/IStorage.MoveElementTo
dev_langs:
- c++
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
- IStorage.MoveElementTo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStorage::MoveElementTo


## -description


The <b>MoveElementTo</b> method copies or moves a substorage or stream from this storage object to another storage object.


## -parameters




### -param pwcsName [in]

Pointer to a wide character null-terminated Unicode string that contains the name of the element in this storage object to be moved or copied.


### -param pstgDest [in]


<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> pointer to the destination storage object.


### -param pwcsNewName [in]

Pointer to a wide character null-terminated unicode string that contains the new name for the element in its new storage object.


### -param grfFlags [in]

Specifies whether the operation should be a move (STGMOVE_MOVE) or a copy (STGMOVE_COPY). See the 
<a href="https://docs.microsoft.com/windows/desktop/api/wtypes/ne-wtypes-stgmove">STGMOVE</a> enumeration.


## -returns



This method can return one of these values.




## -remarks



The <b>IStorage::MoveElementTo</b> method is typically the same as invoking the 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-copyto">IStorage::CopyTo</a> method on the indicated element and then removing the source element. In this case, the 
<b>MoveElementTo</b> method uses only the publicly available functions of the destination storage object to carry out the move.

If the source and destination storage objects have special knowledge about each other's implementation (they could, for example, be different instances of the same implementation), this method can be implemented more efficiently.

Before calling this method, the element to be moved must be closed, and the destination storage must be open. Also, the destination object and element cannot be the same storage object/element name as the source of the move. That is, you cannot move an element to itself.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Stg/istorage-compound-file-implementation">IStorage - Compound File Implementation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-copyto">IStorage::CopyTo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wtypes/ne-wtypes-stgmove">STGMOVE</a>
 

 

