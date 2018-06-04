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

# LIBRARYFOLDERFILTER enumeration


## -description



         Defines options for filtering folder items.
      


## -enum-fields




### -field LFF_FORCEFILESYSTEM


            Return only file system items.
         


### -field LFF_STORAGEITEMS


            Return items that can be bound to an IStorage object.
         


### -field LFF_ALLITEMS


            Return all items.
         


## -remarks



<h3><a id="Used_By"></a><a id="used_by"></a><a id="USED_BY"></a>Used By</h3>

         The <b>LIBRARYFOLDERFILTER</b> enumeration is used by the following methods and functions.
         

<ul>
<li>
<a href="https://msdn.microsoft.com/19abc4f9-5123-4dd9-9606-21b52e28854b">IShellLibrary::GetFolders</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a>
 

 

