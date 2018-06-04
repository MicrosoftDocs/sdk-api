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

# IFolderView::GetCurrentViewMode


## -description


Gets an address containing a value representing the folder's current view mode.


## -parameters




### -param pViewMode [out]

Type: <b>UINT*</b>

A pointer to a memory location at which to store the folder's current view mode. The value at that address is one of the following <a href="https://msdn.microsoft.com/16b92115-6e7d-41d3-960d-6783d779224c">FOLDERVIEWMODE</a> values.





#### FVM_ICON

Medium icons



#### FVM_SMALLICON

Small icons



#### FVM_LIST

List view without details



#### FVM_DETAILS

Show details (size, type, last modification date)



#### FVM_THUMBNAIL

Thumbnail view



#### FVM_TILE

Large icons



#### FVM_THUMBSTRIP

Filmstrip view


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/69d18b4f-3a68-420c-a184-05c2f69a5ec6">GetCurrentInfo</a>



<a href="https://msdn.microsoft.com/3bc2615e-f07c-4959-b89e-bbbd2bf45a94">IFolderView</a>



<a href="https://msdn.microsoft.com/7ca42567-7bb9-41e1-8f2a-5f6d0309c636">IFolderView::SetCurrentViewMode</a>
 

 

