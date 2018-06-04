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

# SToolbarItem structure


## -description


Deprecated. Data used in <a href="https://msdn.microsoft.com/9bce71ca-189e-4072-9acf-10c8b3a34c5c">IBrowserService2::_GetToolbarItem</a>, <a href="https://msdn.microsoft.com/a1c271b2-d567-43b4-966e-0eea597f004b">IBrowserService2::v_MayGetNextToolbarFocus</a>, and <a href="https://msdn.microsoft.com/4a69c3f4-49e0-4a06-8cf2-dc8db640f58f">IBrowserService2::_SetFocus</a> to define a toolbar item.


## -struct-fields




### -field ptbar

Type: <b><a href="https://msdn.microsoft.com/9e80fd5e-f57d-4801-b198-73b8f5ffff6e">IDockingWindow</a>*</b>

The <a href="https://msdn.microsoft.com/9e80fd5e-f57d-4801-b198-73b8f5ffff6e">IDockingWindow</a> of the item's particular toolbar.


### -field rcBorderTool

Type: <b><a href="https://msdn.microsoft.com/f86321d9-5706-4641-b3c9-981a8acacff6">BORDERWIDTHS</a></b>

A <a href="https://msdn.microsoft.com/f86321d9-5706-4641-b3c9-981a8acacff6">BORDERWIDTHS</a> structure that contains the dimensions of the item, including its borders.


### -field pwszItem

Type: <b>LPWSTR</b>

A pointer to a buffer that contains the name of the toolbar item as a Unicode string.


### -field fShow

Type: <b>BOOL</b>

<b>TRUE</b> if the toolbar item is currently visible; otherwise, <b>FALSE</b>.


### -field hMon

Type: <b>HMONITOR</b>

The handle of the monitor on which the toolbar item appears.

