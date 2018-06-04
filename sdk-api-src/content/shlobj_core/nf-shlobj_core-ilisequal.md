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

# ILIsEqual function


## -description


Tests whether two <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structures are equal in a binary comparison.


## -parameters




### -param pidl1 [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

The first <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure.


### -param pidl2 [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

The second <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the two structures are equal, <b>FALSE</b> otherwise.




## -remarks



<b>ILIsEqual</b> performs a binary comparison of the item data. It is possible for two <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structures to differ at the binary level while referring to the same item. <a href="https://msdn.microsoft.com/54d805cc-5396-4892-9347-cafc2d90779f">IShellFolder::CompareIDs</a> should be used to perform a non-binary comparison.



