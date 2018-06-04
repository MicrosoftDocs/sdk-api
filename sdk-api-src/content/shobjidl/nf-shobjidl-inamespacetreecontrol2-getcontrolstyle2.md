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

# INameSpaceTreeControl2::GetControlStyle2


## -description


Gets the extended display styles set for the namespace object's treeview controls.


## -parameters




### -param nstcsMask [in]

Type: <b><a href="https://msdn.microsoft.com/0bfa6900-71c0-44b7-8157-662bee58e6c9">NSTCSTYLE2</a></b>

One or more of the <a href="https://msdn.microsoft.com/0bfa6900-71c0-44b7-8157-662bee58e6c9">NSTCSTYLE2</a> constants that specify the values for which the method should retrieve the current settings.


### -param pnstcsStyle [out]

Type: <b><a href="https://msdn.microsoft.com/0bfa6900-71c0-44b7-8157-662bee58e6c9">NSTCSTYLE2</a>*</b>

Pointer to a value that, when this method returns successfully, receives the values requested in <i>nstcsMask</i>. If the bit that represents the individual <a href="https://msdn.microsoft.com/0bfa6900-71c0-44b7-8157-662bee58e6c9">NSTCSTYLE2</a> value is 0, that value is not set. If the value is 1, it is the current setting. Bit values in positions not specifically requested in <i>nstcsMask</i> do not necessarily reflect the current settings and should not be used.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5f9514db-35fe-44c7-9324-d69022628913">INameSpaceTreeControl2</a>



<a href="https://msdn.microsoft.com/5305d7ba-e37f-4f95-8ae2-e0532012cb1e">INameSpaceTreeControl2::GetControlStyle</a>



<a href="https://msdn.microsoft.com/17d54fa9-ff5c-4fca-a7a6-7ecd4a58c7b9">INameSpaceTreeControl2::SetControlStyle2</a>



<a href="https://msdn.microsoft.com/0bfa6900-71c0-44b7-8157-662bee58e6c9">NSTCSTYLE2</a>
 

 

