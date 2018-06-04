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
 

 

