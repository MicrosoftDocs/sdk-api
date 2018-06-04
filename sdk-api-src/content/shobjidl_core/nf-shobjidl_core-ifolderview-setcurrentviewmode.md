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

# IFolderView::SetCurrentViewMode


## -description


Sets the selected folder's view mode.


## -parameters




### -param ViewMode [in]

Type: <b>UINT</b>

One of the following values from the <a href="https://msdn.microsoft.com/16b92115-6e7d-41d3-960d-6783d779224c">FOLDERVIEWMODE</a> enumeration.



#### FVM_ICON

Medium icons



#### FVM_SMALLICON

Small icons



#### FVM_LIST

List view without details. This view also uses small icons, but they cannot be rearranged as they can be when using <b>FVM_SMALLICON</b>.



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




<a href="https://msdn.microsoft.com/62d71bca-d2cb-4668-b0bf-2e53756f2cd9">CreateViewWindow</a>



<a href="https://msdn.microsoft.com/3bc2615e-f07c-4959-b89e-bbbd2bf45a94">IFolderView</a>



<a href="https://msdn.microsoft.com/e8f69203-f0b4-4537-980c-8e5bbdb49aab">IFolderView::GetCurrentViewMode</a>
 

 

