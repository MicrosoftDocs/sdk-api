---
UID: NE:wincodec.WICHeifProperties
title: WICHeifProperties (wincodec.h)
description: Specifies the properties of a High Efficiency Image Format (HEIF) image.
helpviewer_keywords: ["WICHeifOrientation","WICHeifProperties","WICHeifProperties enumeration [Windows Imaging Component]","wic.wicheifproperties","wincodec/WICHeifOrientation","wincodec/WICHeifProperties"]
old-location: wic\wicheifproperties.htm
tech.root: wic
ms.assetid: 171A2EDE-7545-4AC3-B3AC-3A65A22746E5
ms.date: 12/05/2018
ms.keywords: WICHeifOrientation, WICHeifProperties, WICHeifProperties enumeration [Windows Imaging Component], wic.wicheifproperties, wincodec/WICHeifOrientation, wincodec/WICHeifProperties
f1_keywords:
- wincodec/WICHeifProperties
dev_langs:
- c++
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
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
- Wincodec.h
api_name:
- WICHeifProperties
targetos: Windows
req.typenames: WICHeifProperties
req.redist: 
ms.custom: 19H1
---

# WICHeifProperties enumeration


## -description


Specifies the properties of a High Efficiency Image Format (HEIF) image.


## -enum-fields




### -field WICHeifOrientation

[VT_UI2] Indicates the orientation of the image.

The value of this property uses the same numbering scheme as the <a href="https://docs.microsoft.com/windows/desktop/properties/props-system-photo-orientation">System.Photo.Orientation</a> property. For example, a value of 1 (PHOTO_ORIENTATION_NORMAL) indicates a 0 degree rotation.


### -field WICHeifProperties_FORCE_DWORD



