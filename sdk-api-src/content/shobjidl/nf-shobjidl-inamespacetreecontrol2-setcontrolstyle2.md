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

# INameSpaceTreeControl2::SetControlStyle2


## -description


Sets the extended display styles for the namespace object's treeview controls.


## -parameters




### -param nstcsMask [in]

Type: <b><a href="https://msdn.microsoft.com/0bfa6900-71c0-44b7-8157-662bee58e6c9">NSTCSTYLE2</a></b>

One or more of the <a href="https://msdn.microsoft.com/0bfa6900-71c0-44b7-8157-662bee58e6c9">NSTCSTYLE2</a> constants that specify the styles for which the method should set new values.


### -param nstcsStyle [in]

Type: <b><a href="https://msdn.microsoft.com/0bfa6900-71c0-44b7-8157-662bee58e6c9">NSTCSTYLE2</a></b>

A bitmap that contains the new values for the styles specified in <i>nstcsMask</i>. If the bit that represents the individual <a href="https://msdn.microsoft.com/0bfa6900-71c0-44b7-8157-662bee58e6c9">NSTCSTYLE2</a> value is 0, that style is not used. If the value is 1, the style is applied to the treeview. Styles in positions not specified in <i>nstcsMask</i> are left at their current setting regardless of their bit's value in this bitmap.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5f9514db-35fe-44c7-9324-d69022628913">INameSpaceTreeControl2</a>



<a href="https://msdn.microsoft.com/1c96d936-2a79-491b-8e1e-2dd0e71aba10">INameSpaceTreeControl2::GetControlStyle2</a>



<a href="https://msdn.microsoft.com/20a212e2-13e8-4e17-a8d3-78fff2a1fafb">INameSpaceTreeControl2::SetControlStyle</a>



<a href="https://msdn.microsoft.com/0bfa6900-71c0-44b7-8157-662bee58e6c9">NSTCSTYLE2</a>
 

 

