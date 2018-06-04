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

# ILFree function


## -description


Frees an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure allocated by the Shell.


## -parameters




### -param pidl [in]

Type: <b>PIDLIST_RELATIVE</b>

A pointer to the <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure to be freed. This parameter can be <b>NULL</b>.


## -returns



This function does not return a value.




## -remarks



<b>ILFree</b> is often used with <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structures allocated by one of the other IL functions, but it can be used to free any such structure returned by the Shell—for example, the <b>ITEMIDLIST</b> structure returned by <a href="https://msdn.microsoft.com/2cf3a6d2-d3f7-423d-80b1-f530b268190c">SHBrowseForFolder</a> or used in a call to <a href="https://msdn.microsoft.com/6fcac066-1ab0-443a-9994-b68ead3bbc20">SHGetFolderLocation</a>.

<div class="alert"><b>Note</b>  When using Windows 2000 or later, use <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> rather than <b>ILFree</b>. <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structures are always allocated with the Component Object Model (COM) task allocator on those platforms.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/d1bb5993-fe23-42d4-a2c5-8e54e6e37d09">ILAppendID</a>



<a href="https://msdn.microsoft.com/90689575-3308-4817-ae8c-380fa5f55c88">ILClone</a>



<a href="https://msdn.microsoft.com/931df0c7-6acb-4c49-aa2b-464255e97347">ILCloneFirst</a>



<a href="https://msdn.microsoft.com/29eb1e1f-b7ac-4b72-8fce-a4388d7edfcc">ILCombine</a>
 

 

