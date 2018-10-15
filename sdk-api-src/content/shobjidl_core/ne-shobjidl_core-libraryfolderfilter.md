---
UID: NE:shobjidl_core.LIBRARYFOLDERFILTER
title: LIBRARYFOLDERFILTER
author: windows-sdk-content
description: Defines options for filtering folder items.
old-location: shell\LIBRARYFOLDERFILTER.htm
tech.root: shell
ms.assetid: 8bcb8ee7-14a9-411e-978d-ddeed83d8392
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: LFF_ALLITEMS, LFF_FORCEFILESYSTEM, LFF_STORAGEITEMS, LIBRARYFOLDERFILTER, LIBRARYFOLDERFILTER enumeration [Windows Shell], _shell_LIBRARYFOLDERFILTER, shell.LIBRARYFOLDERFILTER, shobjidl_core/LFF_ALLITEMS, shobjidl_core/LFF_FORCEFILESYSTEM, shobjidl_core/LFF_STORAGEITEMS, shobjidl_core/LIBRARYFOLDERFILTER
ms.prod: windows
ms.technology: windows-sdk
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
 - LIBRARYFOLDERFILTER
product: Windows
targetos: Windows
req.typenames: LIBRARYFOLDERFILTER
req.redist: 
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
 

 

