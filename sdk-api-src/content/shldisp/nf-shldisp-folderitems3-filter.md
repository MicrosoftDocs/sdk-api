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

# FolderItems3::Filter


## -description


Sets a wildcard filter to apply to the items returned.


## -parameters




### -param grfFlags [in]

Type: <b>Integer</b>

This parameter can be one of the flags listed in <a href="https://msdn.microsoft.com/a46845bf-ade6-4366-8a73-6dc960fd7722">SHCONTF</a>.


### -param bstrFileSpec






#### - bstrFilter [in]

Type: <b><a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a></b>

A filter string that specifies what should be listed in the <a href="https://msdn.microsoft.com/b99201b3-95e8-4ddd-b338-dee8d107d0a0">FolderItems</a> collection.


## -see-also




<a href="https://msdn.microsoft.com/38c0e049-2f9f-43bc-8bf2-1b7becf16e66">FolderItem</a>



<a href="https://msdn.microsoft.com/0ca0efb3-6831-4561-9fd1-6d0b62704931">FolderItems2</a>



<a href="https://msdn.microsoft.com/e8ffe325-e6ae-4fa0-9824-22721c2d97c8">FolderItems3</a>
 

 

