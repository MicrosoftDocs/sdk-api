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

# ISearchFolderItemFactory::SetIconSize


## -description


Sets the search folder icon size, as specified. The default settings are based on the <code>FolderTypeID</code> which is set by the <a href="https://msdn.microsoft.com/a9b09dc6-751e-4d5f-b016-0b26c15c68f6">ISearchFolderItemFactory::SetFolderTypeID</a> method.


## -parameters




### -param iIconSize [in]

Type: <b>int</b>

The icon size.


## -returns



Type: <b>HRESULT</b>

Returns a success value if successful, or an error value otherwise.



