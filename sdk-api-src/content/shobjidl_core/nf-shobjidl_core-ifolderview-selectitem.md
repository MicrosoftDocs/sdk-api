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

# IFolderView::SelectItem


## -description


Selects an item in the folder's view.


## -parameters




### -param iItem [in]

Type: <b>int</b>

The index of the item to select in the folder's view.


### -param dwFlags [in]

Type: <b>DWORD</b>

One of the <a href="https://msdn.microsoft.com/3b0a7ec3-f365-48ec-86b0-ffd4c345deaf">_SVSIF</a> constants that specify the type of selection to apply.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3bc2615e-f07c-4959-b89e-bbbd2bf45a94">IFolderView</a>



<a href="https://msdn.microsoft.com/86416704-c2e3-4782-a566-b49cbd0e7696">IFolderView::GetSelectionMarkedItem</a>



<a href="https://msdn.microsoft.com/1263bba8-63c8-4630-ab59-bb4ae10061fc">IFolderView::SelectAndPositionItems</a>



<a href="https://msdn.microsoft.com/5c34c05e-175c-43cb-9fbb-2eb3e2b39f6f">SelectItem</a>
 

 

