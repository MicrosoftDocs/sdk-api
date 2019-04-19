---
UID: NE:shobjidl_core.LIBRARYSAVEFLAGS
title: LIBRARYSAVEFLAGS (shobjidl_core.h)
author: windows-sdk-content
description: Specifies the options for handling a name collision when saving a library.
old-location: shell\LIBRARYSAVEFLAGS.htm
tech.root: shell
ms.assetid: cae52226-0030-457b-aebf-00aaf860243d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: LIBRARYSAVEFLAGS, LIBRARYSAVEFLAGS enumeration [Windows Shell], LSF_FAILIFTHERE, LSF_MAKEUNIQUENAME, LSF_OVERRIDEEXISTING, _shell_LIBRARYSAVEFLAGS, shell.LIBRARYSAVEFLAGS, shobjidl_core/LIBRARYSAVEFLAGS, shobjidl_core/LSF_FAILIFTHERE, shobjidl_core/LSF_MAKEUNIQUENAME, shobjidl_core/LSF_OVERRIDEEXISTING
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
 - LIBRARYSAVEFLAGS
product: Windows
targetos: Windows
req.typenames: LIBRARYSAVEFLAGS
req.redist: 
ms.custom: 19H1
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
 

 

