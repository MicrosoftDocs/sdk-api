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

# tagLVITEMINDEX structure


## -description


Contains index information about a list-view item.


## -struct-fields




### -field iItem

Type: <b>int</b>

The index of the item.


### -field iGroup

Type: <b>int</b>

The index of the group the item belongs to.


## -remarks



This structure is used with the <a href="https://msdn.microsoft.com/eaf8e840-c057-41d4-bfc5-fdd66be8c6be">ListView_GetItemIndexRect</a>, <a href="https://msdn.microsoft.com/94a8e032-37c8-4ba0-99fe-6c2d77f0f2ee">ListView_GetNextItemIndex</a>, and <a href="https://msdn.microsoft.com/f1531cbd-d04a-4a12-9f29-d65122a1fb2c">ListView_SetItemIndexState</a> macros. It is also used with the <a href="https://msdn.microsoft.com/17704d24-c029-4d41-b198-04d1e78698e0">LVM_GETITEMINDEXRECT</a>, <a href="https://msdn.microsoft.com/84cfeb24-83b5-4028-a4ca-97c39ae3c817">LVM_GETNEXTITEMINDEX</a>, and <a href="https://msdn.microsoft.com/9fea6420-320a-4d2a-84b5-7923fbb14655">LVM_SETITEMINDEXSTATE</a> messages.



