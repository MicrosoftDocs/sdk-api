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

# ILIsAligned function


## -description


Verifies whether a constant <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> is aligned on a pointer boundary, which is a <b>DWORD</b> on 32-bit architectures and a <b>QWORD</b> on 64-bit architectures.


## -parameters




### -param pidl [in]

Type: <b>PCUIDLIST_RELATIVE</b>

A constant PIDL relative to a parent folder that is being checked for alignment.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if aligned; otherwise, <b>FALSE</b>.




## -remarks



For use where STRICT_TYPED_ITEMIDS is defined.



