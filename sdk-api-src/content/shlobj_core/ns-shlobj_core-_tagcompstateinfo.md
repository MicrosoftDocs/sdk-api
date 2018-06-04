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

# _tagCOMPSTATEINFO structure


## -description


Used by Windows 2000 to hold information about a component's state.


## -struct-fields




### -field dwSize

Type: <b>DWORD</b>

The size of the structure.


### -field iLeft

Type: <b>int</b>

The left edge of the top-left corner in screen coordinates.


### -field iTop

Type: <b>int</b>

The top of the top-left corner in screen coordinates.


### -field dwWidth

Type: <b>DWORD</b>

The width, in pixels.


### -field dwHeight

Type: <b>DWORD</b>

The height, in pixels.


### -field dwItemState

Type: <b>DWORD</b>

The state of the component.



#### IS_NORMAL

Normal screen.



#### IS_FULLSCREEN

Full screen.



#### IS_SPLIT

Split screen.

