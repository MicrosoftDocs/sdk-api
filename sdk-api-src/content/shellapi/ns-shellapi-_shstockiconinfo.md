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

# _SHSTOCKICONINFO structure


## -description


Receives information used to retrieve a stock Shell icon. This structure is used in a call <a href="https://msdn.microsoft.com/c08b1a53-e67c-4ed0-a9c6-d000c448e182">SHGetStockIconInfo</a>.


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

The size of this structure, in bytes.


### -field hIcon

Type: <b>HICON</b>

When <a href="https://msdn.microsoft.com/c08b1a53-e67c-4ed0-a9c6-d000c448e182">SHGetStockIconInfo</a> is called with the SHGSI_ICON flag, this member receives a handle to the icon.


### -field iSysImageIndex

Type: <b>int</b>

When <a href="https://msdn.microsoft.com/c08b1a53-e67c-4ed0-a9c6-d000c448e182">SHGetStockIconInfo</a> is called with the SHGSI_SYSICONINDEX flag, this member receives the index of the image in the system icon cache.


### -field iIcon

Type: <b>int</b>

When <a href="https://msdn.microsoft.com/c08b1a53-e67c-4ed0-a9c6-d000c448e182">SHGetStockIconInfo</a> is called with the SHGSI_ICONLOCATION flag, this member receives the index of the icon in the resource whose path is received in <b>szPath</b>.


### -field szPath

Type: <b>WCHAR[MAX_PATH]</b>

When <a href="https://msdn.microsoft.com/c08b1a53-e67c-4ed0-a9c6-d000c448e182">SHGetStockIconInfo</a> is called with the SHGSI_ICONLOCATION flag, this member receives the path of the resource that contains the icon. The index of the icon within the resource is received in <b>iIcon</b>.


## -see-also




<a href="https://msdn.microsoft.com/c08b1a53-e67c-4ed0-a9c6-d000c448e182">SHGetStockIconInfo</a>
 

 

