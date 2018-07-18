---
UID: NF:objidl.IStorage.DestroyElement
title: IStorage::DestroyElement
author: windows-sdk-content
description: Removes the specified storage or stream from this storage object.
old-location: stg\istorage_destroyelement.htm
old-project: stg
ms.assetid: 70ad7f8c-15ea-42f1-ac18-006bc6ad5e81
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: DestroyElement, DestroyElement method [Structured Storage], DestroyElement method [Structured Storage],IStorage interface, IStorage interface [Structured Storage],DestroyElement method, IStorage.DestroyElement, IStorage::DestroyElement, _stg_istorage_destroyelement, objidl/IStorage::DestroyElement, stg.istorage_destroyelement
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
 - IStorage.DestroyElement
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# IStorage::DestroyElement


## -description


The 
<b>DestroyElement</b> method
			 removes the specified storage or stream from this storage object.


## -parameters




### -param pwcsName [in]

A pointer to a wide character null-terminated Unicode string that contains the name of the storage or stream to be removed.


## -returns



This method can return one of these values.




## -remarks



The 
<b>DestroyElement</b> method deletes a substorage or stream from the current storage object. After a successful call to 
<b>DestroyElement</b>, any open instance of the destroyed element from the parent storage becomes invalid.

If a storage object is opened in the transacted mode, destruction of an element requires that the call to 
<b>DestroyElement</b> be followed by a call to <a href="https://msdn.microsoft.com/72831f2c-1e07-429b-af4c-2aaced3f3888">IStorage::Commit</a>.

<div class="alert"><b>Note</b>  The <b>DestroyElement</b> method does not shrink the directory stream.  It only marks the deleted directory entry as invalid.  Invalid entries are reused when creating a new storage or stream.  <p class="note">For content streams, the deleted stream sectors are marked as free. If the free sectors are at the end of the file, the document file should shrink.  To compact a document file, call <b>IStorage::CopyTo</b> on the root storage object and copy to a new storage object.

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/2a2253f6-d3d3-403e-a9ba-53a541c7a31e">IStorage - Compound File Implementation</a>
 

 

