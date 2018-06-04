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

# tagTPMPARAMS structure


## -description


Contains extended parameters for the <a href="https://msdn.microsoft.com/86b8f21b-0dfe-462e-a34a-c80ee5c1d185">TrackPopupMenuEx</a> function.


## -struct-fields




### -field cbSize

Type: <b>UINT</b>

The size of structure, in bytes. 


### -field rcExclude

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a></b>

The rectangle to be excluded when positioning the window, in screen coordinates. 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/86b8f21b-0dfe-462e-a34a-c80ee5c1d185">TrackPopupMenuEx</a>
 

 

