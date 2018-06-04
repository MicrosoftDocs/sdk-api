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

# GetMenuCheckMarkDimensions function


## -description


Retrieves the dimensions of the default check-mark bitmap. The system displays this bitmap next to selected menu items. Before calling the <a href="https://msdn.microsoft.com/7c0fb026-52ca-4ac6-bb94-1e72431b6056">SetMenuItemBitmaps</a> function to replace the default check-mark bitmap for a menu item, an application must determine the correct bitmap size by calling <b>GetMenuCheckMarkDimensions</b>. 
<div class="alert"><b>Note</b>  The <b>GetMenuCheckMarkDimensions</b> function is included only for compatibility with 16-bit versions of Windows. Applications should use the <a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a> function with the <b>CXMENUCHECK</b> and <b>CYMENUCHECK</b> values to retrieve the bitmap dimensions.</div><div> </div>

## -parameters






## -returns



Type: <b>LONG</b>

The return value specifies the height and width, in pixels, of the default check-mark bitmap. The high-order word contains the height; the low-order word contains the width. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/7c0fb026-52ca-4ac6-bb94-1e72431b6056">SetMenuItemBitmaps</a>
 

 

