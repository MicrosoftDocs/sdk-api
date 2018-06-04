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

# DISPLAYCONFIG_SCALING enumeration


## -description


The DISPLAYCONFIG_SCALING enumeration specifies the scaling transformation applied to content displayed on a video present network (VidPN) present path.


## -enum-fields




### -field DISPLAYCONFIG_SCALING_IDENTITY

Indicates the identity transformation; the source content is presented with no change. This transformation is available only if the path's source mode has the same spatial resolution as the path's target mode.


### -field DISPLAYCONFIG_SCALING_CENTERED

Indicates the centering transformation; the source content is presented unscaled, centered with respect to the spatial resolution of the target mode.


### -field DISPLAYCONFIG_SCALING_STRETCHED

Indicates the content is scaled to fit the path's target.


### -field DISPLAYCONFIG_SCALING_ASPECTRATIOCENTEREDMAX

Indicates the aspect-ratio centering transformation. 


### -field DISPLAYCONFIG_SCALING_CUSTOM

Indicates that the caller requests a custom scaling that the caller cannot describe with any of the other DISPLAYCONFIG_SCALING_XXX values. Only a hardware vendor's value-add application should use DISPLAYCONFIG_SCALING_CUSTOM, because the value-add application might require a private interface to the driver. The application can then use DISPLAYCONFIG_SCALING_CUSTOM to indicate additional context for the driver for the custom value on the specified path. 


### -field DISPLAYCONFIG_SCALING_PREFERRED

Indicates that the caller does not have any preference for the scaling. The <a href="https://msdn.microsoft.com/library/windows/hardware/ff569533">SetDisplayConfig</a> function will use the scaling value that was last saved in the database for the path. If such a scaling value does not exist, <b>SetDisplayConfig</b> will use the default scaling for the computer. For example, stretched (DISPLAYCONFIG_SCALING_STRETCHED) for tablet computers and aspect-ratio centered (DISPLAYCONFIG_SCALING_ASPECTRATIOCENTEREDMAX) for non-tablet computers. 


### -field DISPLAYCONFIG_SCALING_FORCE_UINT32

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. You should not use this value. 


## -remarks



For more information about scaling, see <a href="https://msdn.microsoft.com/e27c7510-45b0-46e6-878f-b901cdd1cd57">Scaling the Desktop Image</a>. 



