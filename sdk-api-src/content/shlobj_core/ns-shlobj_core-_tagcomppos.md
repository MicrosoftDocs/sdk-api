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

# _tagCOMPPOS structure


## -description


Holds information about a component's position and size.


## -struct-fields




### -field dwSize

Type: <b>DWORD</b>

The size of the structure.


### -field iLeft

Type: <b>int</b>

The left edge of the top-left corner in screen coordinates. Set to COMPONENT_DEFAULT_LEFT to let the Shell decide the position.


### -field iTop

Type: <b>int</b>

The top of the top-left corner in screen coordinates. Set to COMPONENT_DEFAULT_TOP to let the Shell decide the position.


### -field dwWidth

Type: <b>DWORD</b>

The width, in pixels.


### -field dwHeight

Type: <b>DWORD</b>

The height, in pixels.


### -field izIndex

Type: <b>int</b>

The z-order of the component.


### -field fCanResize

Type: <b>BOOL</b>

Set to <b>TRUE</b> if the component is resizable, <b>FALSE</b> if not.


### -field fCanResizeX

Type: <b>BOOL</b>

Set to <b>TRUE</b> if the component is resizable in the x direction, <b>FALSE</b> if not.


### -field fCanResizeY

Type: <b>BOOL</b>

Set to <b>TRUE</b> if the component is resizable in the y direction, <b>FALSE</b> if not.


### -field iPreferredLeftPercent

Type: <b>int</b>

The left edge of the upper-left corner as a percentage of screen width.


### -field iPreferredTopPercent

Type: <b>int</b>

The top of the upper-left corner as a percentage of screen width.

