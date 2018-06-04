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

# CreateIFELanguageInstance function


## -description


Returns a pointer to an   <a href="https://msdn.microsoft.com/9EE1BD9E-2D58-4720-841C-39865375BFE0">IFELanguage</a> interface.


## -parameters




### -param clsid [in]

Reserved. Must be set to <b>NULL</b>.


### -param ppvObj [out]

Address of the pointer variable that receives the <a href="https://msdn.microsoft.com/9EE1BD9E-2D58-4720-841C-39865375BFE0">IFELanguage</a> interface pointer of the object created.


## -returns



<b>S_OK</b> if successful, otherwise an OLE-defined error code.



