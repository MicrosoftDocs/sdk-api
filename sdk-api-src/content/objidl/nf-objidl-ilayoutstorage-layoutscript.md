---
UID: NF:objidl.ILayoutStorage.LayoutScript
title: ILayoutStorage::LayoutScript
author: windows-sdk-content
description: The LayoutScript method provides explicit directions for reordering the storages, streams, and controls in a compound file to match the order in which they are accessed during the download.
old-location: stg\ilayoutstorage_layoutscript.htm
old-project: Stg
ms.assetid: 22ae3485-15d9-47e4-988e-fb760e67595b
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: ILayoutStorage interface [Structured Storage],LayoutScript method, ILayoutStorage.LayoutScript, ILayoutStorage::LayoutScript, LayoutScript, LayoutScript method [Structured Storage], LayoutScript method [Structured Storage],ILayoutStorage interface, _stg_ilayoutstorage_layoutscript, objidl/ILayoutStorage::LayoutScript, stg.ilayoutstorage_layoutscript
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
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
 - ILayoutStorage.LayoutScript
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ILayoutStorage::LayoutScript


## -description



			The <b>LayoutScript</b> method provides explicit directions for reordering the storages, streams, and controls in a compound file to match the order in which they are accessed during the download.


## -parameters




### -param pStorageLayout [in]

Pointer to an array of 
<a href="https://msdn.microsoft.com/1e4fb36d-077b-44bd-ab6e-8c122ec95a46">StorageLayout</a> structures.


### -param nEntries [in]

Number of entries in the array of 
<a href="https://msdn.microsoft.com/1e4fb36d-077b-44bd-ab6e-8c122ec95a46">StorageLayout</a> structures.


### -param glfInterleavedFlag [in]

Reserved for future use.


## -returns




						This function supports the standard return values E_OUTOFMEMORY, E_UNEXPECTED, E_INVALIDARG, and E_FAIL, as well as the following:




## -remarks



To provide explicit layout instructions, the application calls <b>ILayoutStorage::LayoutScript</b>, passing an array of 
<a href="https://msdn.microsoft.com/1e4fb36d-077b-44bd-ab6e-8c122ec95a46">StorageLayout</a> structures. Each structure defines a single storage or stream data block and specifies where the block is to be written in the 
<a href="https://msdn.microsoft.com/bb2c5d0d-8dc8-4844-9a20-ef8e4def5731">ILockBytes</a> byte array.

An application can combine scripted layout with monitoring, as the structure of a particular compound file may dictate.

When the optimal data-layout pattern of an entire compound file has been determined, the application calls 
<a href="https://msdn.microsoft.com/5db3a26c-595a-4c9b-bb6d-b170eb9864df">ILayoutStorage::ReLayoutDocfile</a> to restructure the compound file to match the order in which its data sectors were accessed.




## -see-also




<a href="https://msdn.microsoft.com/5db3a26c-595a-4c9b-bb6d-b170eb9864df">ILayoutStorage::ReLayoutDocfile</a>



<a href="https://msdn.microsoft.com/bb2c5d0d-8dc8-4844-9a20-ef8e4def5731">ILockBytes</a>



<a href="https://msdn.microsoft.com/1e4fb36d-077b-44bd-ab6e-8c122ec95a46">StorageLayout</a>
 

 

