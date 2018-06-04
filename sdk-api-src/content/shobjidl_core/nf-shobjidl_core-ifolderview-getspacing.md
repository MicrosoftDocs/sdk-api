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

# IFolderView::GetSpacing


## -description


Gets a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure containing the width (x) and height (y) dimensions, including the surrounding white space, of an item.


## -parameters




### -param ppt [in, out]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a>*</b>

A pointer to an existing structure to be filled with the current sizing dimensions of the items in the folder's view.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



As an example, consider an icon measuring 75 pixels by 70 pixels, with its upper-left corner located at pixel (0,0). Note that this measurement includes both the visible graphic and its surrounding buffer area. <b>IFolderView::GetSpacing</b> would return a pointer to a POINT structure containing an x value of 75 and a y value of 70. If you were using this information to avoid overlap, the next icon in line to the right would be placed with its upper-left corner at pixel (75,0). Similarly, the next icon below would be placed at pixel (0,70).




## -see-also




<a href="https://msdn.microsoft.com/3bc2615e-f07c-4959-b89e-bbbd2bf45a94">IFolderView</a>



<a href="https://msdn.microsoft.com/eb5f2dd6-1257-4cfc-a222-88e6c3b524ce">IFolderView::GetDefaultSpacing</a>
 

 

