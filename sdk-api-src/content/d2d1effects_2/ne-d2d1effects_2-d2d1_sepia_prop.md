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



