---
UID: NE:d2d1effects_2.D2D1_STRAIGHTEN_PROP
title: D2D1_STRAIGHTEN_PROP
author: windows-sdk-content
description: Identifiers for properties of the Straighten effect.
old-location: direct2d\d2d1_straighten_prop.htm
tech.root: direct2d
ms.assetid: AD22B649-E4FE-41BD-85FE-B000CCB7F48D
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: D2D1_STRAIGHTEN_PROP, D2D1_STRAIGHTEN_PROP enumeration [Direct2D], D2D1_STRAIGHTEN_PROP_ANGLE, D2D1_STRAIGHTEN_PROP_MAINTAIN_SIZE, D2D1_STRAIGHTEN_PROP_SCALE_MODE, d2d1effects_2/D2D1_STRAIGHTEN_PROP, d2d1effects_2/D2D1_STRAIGHTEN_PROP_ANGLE, d2d1effects_2/D2D1_STRAIGHTEN_PROP_MAINTAIN_SIZE, d2d1effects_2/D2D1_STRAIGHTEN_PROP_SCALE_MODE, direct2d.d2d1_straighten_prop
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d2d1effects_2.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1effects_2.h
api_name:
 - D2D1_STRAIGHTEN_PROP
product: Windows
targetos: Windows
req.typenames: D2D1_STRAIGHTEN_PROP
req.redist: 
---

# D2D1_STRAIGHTEN_PROP enumeration


## -description


Identifiers for properties of the <a href="https://msdn.microsoft.com/en-us/library/Dn900462(v=VS.85).aspx">Straighten effect</a>.


## -enum-fields




### -field D2D1_STRAIGHTEN_PROP_ANGLE

The D2D1_STRAIGHTEN_PROP_ANGLE property is a float value that specifies how much the image should be rotated.  The allowed range is -45.0 to 45.0.  The default value is 0.0.


### -field D2D1_STRAIGHTEN_PROP_MAINTAIN_SIZE

The D2D1_STRAIGHTEN_PROP_MAINTAIN_SIZE property is a boolean value that specifies whether the image will be scaled such that the original size is maintained without any invalid regions.
          The default value is True.


### -field D2D1_STRAIGHTEN_PROP_SCALE_MODE

The D2D1_STRAIGHTEN_PROP_SCALE_MODE property is a <a href="https://msdn.microsoft.com/en-us/library/Dn890748(v=VS.85).aspx">D2D1_STRAIGHTEN_SCALE_MODE</a> enumeration value indicating the scaling mode that should be used.


### -field D2D1_STRAIGHTEN_PROP_FORCE_DWORD



