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

# ILAppendID function


## -description


Appends or prepends an <a href="https://msdn.microsoft.com/794c8425-2319-4339-881c-c5083ab05638">SHITEMID</a> structure to an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure.


## -parameters




### -param pidl [in, optional]

Type: <b>PIDLIST_RELATIVE</b>

A pointer to an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure. When the function returns, the <a href="https://msdn.microsoft.com/794c8425-2319-4339-881c-c5083ab05638">SHITEMID</a> structure specified by <i>pmkid</i> is appended or prepended.


### -param pmkid [in]

Type: <b>LPSHITEMID</b>

A pointer to a <a href="https://msdn.microsoft.com/794c8425-2319-4339-881c-c5083ab05638">SHITEMID</a> structure to be appended or prepended to <i>pidl</i>.


### -param fAppend

Type: <b>BOOL</b>

Value that is set to <b>TRUE</b> to append <i>pmkid</i> to <i>pidl</i>. Set this value to <b>FALSE</b> to prepend <i>pmkid</i> to <i>pidl</i>.


## -returns



Type: <b>PIDLIST_RELATIVE</b>

Returns the <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure specified by <i>pidl</i>, with <i>pmkid</i> appended or prepended. Returns <b>NULL</b> on failure.



