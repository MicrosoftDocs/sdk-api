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

# ILNext function


## -description


Retrieves the next <a href="https://msdn.microsoft.com/794c8425-2319-4339-881c-c5083ab05638">SHITEMID</a> structure in an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure.


## -parameters




### -param pidl [in]

Type: <b>PCUIDLIST_RELATIVE</b>

A constant, unaligned, relative PIDL for which the next <a href="https://msdn.microsoft.com/794c8425-2319-4339-881c-c5083ab05638">SHITEMID</a> structure is being retrieved.


## -returns



Type: <b>PCUIDLIST_RELATIVE</b>

When this function returns, contains one of three results: If <i>pidl</i> is valid and not the last <a href="https://msdn.microsoft.com/794c8425-2319-4339-881c-c5083ab05638">SHITEMID</a> in the <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a>, then it contains a pointer to the next <b>ITEMIDLIST</b> structure. If the last <b>ITEMIDLIST</b> structure is passed, it contains <b>NULL</b>, which signals the end of the PIDL. For other values of <i>pidl</i>, the return value is meaningless.




## -remarks



For use where STRICT_TYPED_ITEMIDS is defined.

To verify if the return value is <b>NULL</b>, use <a href="https://msdn.microsoft.com/bb727aad-9c4e-44dc-9c0c-4cbcbf3f9a78">ILIsEmpty</a>.



