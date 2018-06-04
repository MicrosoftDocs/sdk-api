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

# D2D1_CONTRAST_PROP enumeration


## -description


Identifiers for properties of the <a href="https://msdn.microsoft.com/c0cc0f86-f6d4-e951-0cdd-dbad488e0793">Contrast effect</a>.


## -enum-fields




### -field D2D1_CONTRAST_PROP_CONTRAST

The D2D1_CONTRAST_PROP_CONTRAST property is a float value indicating the amount by which to adjust the contrast of the image. Negative values reduce contrast, while positive values increase contrast.  
          Minimum value is -1.0f, maximum value is 1.0f.  The default value for the property is 0.0f.


### -field D2D1_CONTRAST_PROP_CLAMP_INPUT

The D2D1_CONTRAST_PROP_CLAMP_INPUT property is a boolean value indicating whether or not to clamp the input to [0.0, 1.0]. The default value for the property is FALSE.


### -field D2D1_CONTRAST_PROP_FORCE_DWORD




## -see-also




<a href="https://msdn.microsoft.com/A76F6AB8-16E9-45C9-A768-5E4AA072D534">Built-in Effects</a>



<a href="https://msdn.microsoft.com/c0cc0f86-f6d4-e951-0cdd-dbad488e0793">Contrast effect</a>



<a href="https://msdn.microsoft.com/dfe587f9-e92f-4367-a503-edd446a91cb8">CreateEffect</a>
 

 

