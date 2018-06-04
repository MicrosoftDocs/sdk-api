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

# DEFAULTSAVEFOLDERTYPE enumeration


## -description


Specifies the default save location.


## -enum-fields




### -field DSFT_DETECT

The current user determines the save folder. If the current user is the library's owner,  use the private save location (<a href="https://msdn.microsoft.com/51478854-03b2-4e1a-bc07-b9ca7e6cc33d">DSFT_PRIVATE</a>). If the current user is not the library's owner, use the public save location (<a href="https://msdn.microsoft.com/51478854-03b2-4e1a-bc07-b9ca7e6cc33d">DSFT_PUBLIC</a>).


### -field DSFT_PRIVATE

The library's private save location, which can only be accessed by the library's owner.


### -field DSFT_PUBLIC

The library's public save location, which can be accessed by all users.


## -remarks



These values cannot be combined.

<h3><a id="Used_By"></a><a id="used_by"></a><a id="USED_BY"></a>Used By</h3>
<ul>
<li>
<a href="https://msdn.microsoft.com/4bc501b1-2fc4-49ce-a16b-e254a3a40f46">IShellLibrary::GetDefaultSaveFolder</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0c65bd5e-22f4-450b-a1d5-75e564854b5f">IShellLibrary::SetDefaultSaveFolder</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a>
 

 

