---
UID: NE:d2d1effects_2.D2D1_SEPIA_PROP
title: D2D1_SEPIA_PROP
author: windows-sdk-content
description: Identifiers for properties of the Sepia effect.
old-location: direct2d\d2d1_sepia_prop.htm
tech.root: direct2d
ms.assetid: 159897D5-DB46-46B7-A88B-CC57D1AC8DE5
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: D2D1_SEPIA_PROP, D2D1_SEPIA_PROP enumeration [Direct2D], D2D1_SEPIA_PROP_ALPHA_MODE, D2D1_SEPIA_PROP_INTENSITY, d2d1effects_2/D2D1_SEPIA_PROP, d2d1effects_2/D2D1_SEPIA_PROP_ALPHA_MODE, d2d1effects_2/D2D1_SEPIA_PROP_INTENSITY, direct2d.d2d1_sepia_prop
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
 - D2D1_SEPIA_PROP
product: Windows
targetos: Windows
req.typenames: D2D1_SEPIA_PROP
req.redist: 
---

# D2D1_SEPIA_PROP enumeration


## -description


Identifiers for properties of the <a href="https://msdn.microsoft.com/fe321be9-6ade-bd0c-1c66-cc8042e5a5e1">Sepia effect</a>.


## -enum-fields




### -field D2D1_SEPIA_PROP_INTENSITY

The D2D1_SEPIA_PROP_INTENSITY property is a float value indicating the intesity of the sepia effect. The allowed range is 0.0 to 1.0.  The default value is 0.5.


### -field D2D1_SEPIA_PROP_ALPHA_MODE

The D2D1_SEPIA_PROP_ALPHA_MODE property is a <a href="https://msdn.microsoft.com/f1b1e735-2e89-4dc1-9fee-dfb4626ef453">D2D1_ALPHA_MODE</a> enumeration value indicating the alpha mode of the input file.
          See the About Alpha Modes section of the <a href="https://msdn.microsoft.com/09b1f9c6-1780-4733-ac22-9e8c21466b67">Supported Pixel Formats and Alpha Modes</a> topic for additional information..  
          The default value is D2D1_ALPHA_MODE_PREMULTIPLIED.


### -field D2D1_SEPIA_PROP_FORCE_DWORD



