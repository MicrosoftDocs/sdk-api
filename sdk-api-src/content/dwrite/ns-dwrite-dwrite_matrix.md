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

# DWRITE_MATRIX structure


## -description


The <b>DWRITE_MATRIX</b> structure specifies the graphics transform to be applied to rendered glyphs.


## -struct-fields




### -field m11

Type: <b>FLOAT</b>

A value indicating the horizontal scaling / cosine of rotation.


### -field m12

Type: <b>FLOAT</b>

A value indicating the vertical shear / sine of rotation.


### -field m21

Type: <b>FLOAT</b>

A value indicating the horizontal shear / negative sine of rotation.


### -field m22

Type: <b>FLOAT</b>

A value indicating the vertical scaling / cosine of rotation.


### -field dx

Type: <b>FLOAT</b>

A value indicating the horizontal shift (always orthogonal regardless of rotation).


### -field dy

Type: <b>FLOAT</b>

A value indicating the vertical shift (always orthogonal regardless of rotation.)

