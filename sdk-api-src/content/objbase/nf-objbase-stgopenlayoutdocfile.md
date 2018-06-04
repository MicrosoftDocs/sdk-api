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

# StgOpenLayoutDocfile function


## -description


Not supported.

The <b>StgOpenLayoutDocfile</b> function opens a compound file on an 
<a href="https://msdn.microsoft.com/bb2c5d0d-8dc8-4844-9a20-ef8e4def5731">ILockBytes</a> implementation that is capable of monitoring sector data. To call  <b>StgOpenLayoutDocfile</b>, both  DfLayout.dll and DfLayout.lib are required.


<div class="alert"><b>Note</b>  Do not use this function. Use the <a href="https://msdn.microsoft.com/8b25b32b-f739-406a-96e8-dba687c7f055">IStorage::CopyTo</a>  
 method instead. <b>CopyTo</b> can be used to layout a docfile, thus improving performance in most scenarios.</div>
<div> </div>



## -parameters




### -param pwcsDfName [in]

A pointer to the null-terminated Unicode string name of the compound file to be opened.


### -param grfMode [in]

Access mode to use when opening the newly created storage object. Values are taken from the 
<a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM Constants</a>. Be aware that priority mode and exclusions are not supported. The most common access mode is likely to be STGM_DIRECT | STGM_READ | STGM_SHARE_EXCLUSIVE.


### -param reserved [in]

Reserved for future use.


### -param ppstgOpen

TBD




#### - ppStgOpen [out]

A pointer to 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> pointer variable that receives the interface pointer to the root object of the newly created root storage object.


## -returns




						This function supports the standard return values E_OUTOFMEMORY, E_UNEXPECTED, E_INVALIDARG, and E_FAIL, in addition to the following:

The <b>StgOpenLayoutDocfile</b> function can also return any of the error values returned by the 
<a href="https://msdn.microsoft.com/7920bd46-0a8f-42e0-9988-59d85edb64e2">StgOpenStorageOnILockBytes</a> function.




## -remarks



The compound file implementation created by this function exposes the 
<a href="https://msdn.microsoft.com/72201600-4bbb-4346-a13f-927e8463b6ec">ILayoutStorage</a> interface on its root storage. Applications use this interface to express the optimal layout of their compound files in order to download and render data more rapidly over a slow link. 
<b>StgOpenLayoutDocfile</b> returns a pointer to the 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface on the root storage of the newly created compound file. Using this pointer, applications call <b>QueryInterface</b> to obtain a pointer to 
<b>ILayoutStorage</b>.




## -see-also




<a href="https://msdn.microsoft.com/8b25b32b-f739-406a-96e8-dba687c7f055">CopyTo</a>



<a href="https://msdn.microsoft.com/bb2c5d0d-8dc8-4844-9a20-ef8e4def5731">ILockBytes</a>



<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a>



<a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM Constants</a>
 

 

