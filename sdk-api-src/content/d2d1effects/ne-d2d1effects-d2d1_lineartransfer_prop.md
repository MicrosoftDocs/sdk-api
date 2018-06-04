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

# D2D1_LINEARTRANSFER_PROP enumeration


## -description


Identifiers for properties of the <a href="https://msdn.microsoft.com/22DC496E-2958-4726-A74D-B3DE934F507C">Linear transfer effect</a>.


## -enum-fields




### -field D2D1_LINEARTRANSFER_PROP_RED_Y_INTERCEPT

The Y-intercept of the linear function for the Red channel. 
          

The type is FLOAT.

The default is 0.0f.


### -field D2D1_LINEARTRANSFER_PROP_RED_SLOPE

The slope of the linear function for the Red channel.
          

The type is FLOAT.

The default is 1.0f.


### -field D2D1_LINEARTRANSFER_PROP_RED_DISABLE

If you set this to TRUE the effect does not apply the transfer function to the Red channel. 
          If you set this to FALSE the effect applies the RedLinearTransfer function to the Red channel. 
          

The type is BOOL.

The default is FALSE.


### -field D2D1_LINEARTRANSFER_PROP_GREEN_Y_INTERCEPT

The Y-intercept of the linear function for the Green channel. 
          

The type is FLOAT.

The default is 0.0f.


### -field D2D1_LINEARTRANSFER_PROP_GREEN_SLOPE

The slope of the linear function for the Green channel.
          

The type is FLOAT.

The default is 1.0f.


### -field D2D1_LINEARTRANSFER_PROP_GREEN_DISABLE

If you set this to TRUE the effect does not apply the transfer function to the Green channel. 
          If you set this to FALSE the effect applies the GreenLinearTransfer function to the Green channel. 
          

The type is BOOL.

The default is FALSE.


### -field D2D1_LINEARTRANSFER_PROP_BLUE_Y_INTERCEPT

The Y-intercept of the linear function for the Blue channel. 
          

The type is FLOAT.

The default is 0.0f.


### -field D2D1_LINEARTRANSFER_PROP_BLUE_SLOPE

The slope of the linear function for the Blue channel.
          

The type is FLOAT.

The default is 1.0f.


### -field D2D1_LINEARTRANSFER_PROP_BLUE_DISABLE

If you set this to TRUE the effect does not apply the transfer function to the Blue channel. 
          If you set this to FALSE the effect applies the BlueLinearTransfer function to the Blue channel. 
          

The type is BOOL.

The default is FALSE.


### -field D2D1_LINEARTRANSFER_PROP_ALPHA_Y_INTERCEPT

The Y-intercept of the linear function for the Alpha channel. 
          

The type is FLOAT.

The default is 0.0f.


### -field D2D1_LINEARTRANSFER_PROP_ALPHA_SLOPE

The slope of the linear function for the Alpha channel.
          

The type is FLOAT.

The default is 0.0f.


### -field D2D1_LINEARTRANSFER_PROP_ALPHA_DISABLE

If you set this to TRUE the effect does not apply the transfer function to the Alpha channel. 
          If you set this to FALSE the effect applies the AlphaLinearTransfer function to the Alpha channel. 
          

The type is BOOL.

The default is FALSE.


### -field D2D1_LINEARTRANSFER_PROP_CLAMP_OUTPUT

Whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph. 
          The effect clamps the values before it premultiplies the alpha .
          

If you set this to TRUE the effect will clamp the values. If you set this to FALSE, the effect will not clamp the color values, but other effects and 
          the output surface may clamp the values if they are not of high enough precision.

The type is BOOL.

The default is FALSE.


### -field D2D1_LINEARTRANSFER_PROP_FORCE_DWORD



