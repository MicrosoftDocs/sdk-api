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

# LIBRARYSAVEFLAGS enumeration


## -description



         Specifies the options for handling a name collision when saving a library.
      


## -enum-fields




### -field LSF_FAILIFTHERE


            If a library with the same name already exists, the save operation fails.
         


### -field LSF_OVERRIDEEXISTING


            If a library with the same name already exists, the save operation overwrites the existing library.
         


### -field LSF_MAKEUNIQUENAME


            If a library with the same name already exists, the save operation generates a new, unique name for the library.
         


## -remarks



<h3><a id="Used_By"></a><a id="used_by"></a><a id="USED_BY"></a>Used By</h3>
<ul>
<li>
<a href="https://msdn.microsoft.com/2a7de829-f0bc-4ace-aed4-83d0611ae292">IShellLibrary::Save</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3a6fa57f-808d-4893-a01c-f192355f8989">IShellLibrary::SaveInKnownFolder</a>
</li>
<li>
<a href="https://msdn.microsoft.com/953b209b-fd18-49d0-84d3-ad9b815f2a3a">SHSaveLibraryInFolderPath</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a>
 

 

