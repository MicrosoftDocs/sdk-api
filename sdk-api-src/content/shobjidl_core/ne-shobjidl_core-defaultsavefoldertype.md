---
UID: NE:shobjidl_core.DEFAULTSAVEFOLDERTYPE
title: DEFAULTSAVEFOLDERTYPE (shobjidl_core.h)
author: windows-sdk-content
description: Specifies the default save location.
old-location: shell\DEFAULTSAVEFOLDERTYPE.htm
tech.root: shell
ms.assetid: 51478854-03b2-4e1a-bc07-b9ca7e6cc33d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DEFAULTSAVEFOLDERTYPE, DEFAULTSAVEFOLDERTYPE enumeration [Windows Shell], DSFT_DETECT, DSFT_PRIVATE, DSFT_PUBLIC, _shell_DEFAULTSAVEFOLDERTYPE, shell.DEFAULTSAVEFOLDERTYPE, shobjidl_core/DEFAULTSAVEFOLDERTYPE, shobjidl_core/DSFT_DETECT, shobjidl_core/DSFT_PRIVATE, shobjidl_core/DSFT_PUBLIC
ms.topic: enum
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - DEFAULTSAVEFOLDERTYPE
product: Windows
targetos: Windows
req.typenames: DEFAULTSAVEFOLDERTYPE
req.redist: 
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
 

 

