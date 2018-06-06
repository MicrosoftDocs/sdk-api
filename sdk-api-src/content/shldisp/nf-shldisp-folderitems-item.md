---
UID: NF:shldisp.FolderItems.Item
title: FolderItems::Item
author: windows-sdk-content
description: Retrieves the FolderItem object for a specified item in the collection.
old-location: shell\FolderItems_Item.htm
old-project: shell
ms.assetid: 164f823d-12d9-4950-a881-63837c53760d
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: FolderItems object [Windows Shell],Item method, FolderItems.Item, FolderItems::Item, Item, Item method [Windows Shell], Item method [Windows Shell],FolderItems object, _win32_FolderItems_Item, shell.FolderItems_Item
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shldisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AUTOCOMPLETEOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - FolderItems.Item
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# FolderItems::Item


## -description


Retrieves the <a href="https://msdn.microsoft.com/38c0e049-2f9f-43bc-8bf2-1b7becf16e66">FolderItem</a> object for a specified item in the collection.


## -parameters




### -param index




### -param ppid






#### - iIndex [in, optional]

Type: <b>Variant</b>

The zero-based index of the item to retrieve. This value must be less than the value of the <a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a> property.


## -returns



An object reference to the <a href="https://msdn.microsoft.com/38c0e049-2f9f-43bc-8bf2-1b7becf16e66">FolderItem</a> object.




## -see-also




<a href="https://msdn.microsoft.com/b99201b3-95e8-4ddd-b338-dee8d107d0a0">FolderItems</a>
 

 

