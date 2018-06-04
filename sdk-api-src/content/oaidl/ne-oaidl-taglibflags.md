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

# tagLIBFLAGS enumeration


## -description


Defines flags that apply to type libraries.


## -enum-fields




### -field LIBFLAG_FRESTRICTED

The type library is restricted, and should not be displayed to users.


### -field LIBFLAG_FCONTROL

The type library describes controls, and should not be displayed in type browsers intended for nonvisual objects.



### -field LIBFLAG_FHIDDEN

The type library should not be displayed to users, although its use is not restricted. Should be used by controls. Hosts should create a new type library that wraps the control with extended properties.


### -field LIBFLAG_FHASDISKIMAGE

The type library has a disk image.

