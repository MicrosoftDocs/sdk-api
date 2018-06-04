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

# OleQueryLinkFromData function


## -description


Determines whether an OLE linked object (rather than an OLE embedded object) can be created from a clipboard data object.




## -parameters




### -param pSrcDataObject [in]

Pointer to the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface on the clipboard data object from which the object is to be created.


## -returns



Returns S_OK if the <a href="https://msdn.microsoft.com/3eda0cf5-c33d-43cf-ba8a-02a4f6383adc">OleCreateLinkFromData</a> function can be used to create the linked object; otherwise S_FALSE.




## -remarks



The <b>OleQueryLinkFromData</b> function is similar to the <a href="https://msdn.microsoft.com/58fffb8c-9726-4801-84ce-6fb670b865c8">OleQueryCreateFromData</a> function, but determines whether an OLE linked object (rather than an OLE embedded object) can be created from the clipboard data object. If the return value is S_OK, the application can then attempt to create the object with a call to <a href="https://msdn.microsoft.com/3eda0cf5-c33d-43cf-ba8a-02a4f6383adc">OleCreateLinkFromData</a>. A successful return from <b>OleQueryLinkFromData</b> does not, however, guarantee the successful creation of a link.




