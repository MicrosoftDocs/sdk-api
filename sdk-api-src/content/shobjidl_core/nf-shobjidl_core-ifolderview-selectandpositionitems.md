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

# IFolderView::SelectAndPositionItems


## -description


Allows the selection and positioning of items visible in the folder's view.


## -parameters




### -param cidl [in]

Type: <b>UINT</b>

The number of items to select.


### -param apidl [in]

Type: <b>PCUITEMID_CHILD_ARRAY*</b>

A pointer to an array of size <i>cidl</i> that contains the PIDLs of the items.


### -param apt [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a>*</b>

A pointer to an array of <i>cidl</i> structures containing the locations each corresponding element in <i>apidl</i> should be positioned.


### -param dwFlags [in]

Type: <b>DWORD</b>

One of the <a href="https://msdn.microsoft.com/3b0a7ec3-f365-48ec-86b0-ffd4c345deaf">_SVSIF</a> constants that specifies the type of selection to apply.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ab0ebc82-e917-4e3a-864b-fc3bb6280a48">FOLDERVIEWOPTIONS</a>



<a href="https://msdn.microsoft.com/3bc2615e-f07c-4959-b89e-bbbd2bf45a94">IFolderView</a>



<a href="https://msdn.microsoft.com/6db262ea-861b-4bc5-955f-b81945313ea8">IFolderView::SelectItem</a>



<a href="https://msdn.microsoft.com/5c34c05e-175c-43cb-9fbb-2eb3e2b39f6f">SelectItem</a>
 

 

