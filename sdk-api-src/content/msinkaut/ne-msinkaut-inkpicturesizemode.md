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

# InkPictureSizeMode enumeration


## -description



          Specifies how the picture behaves inside the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control.
          
        

The mode is set by using the <a href="https://msdn.microsoft.com/3ce10b92-80d4-4517-92cb-eff10fc8c0ba">SizeMode</a> property and is applied to the picture set with the <a href="https://msdn.microsoft.com/c07433f2-d32c-4b6f-ad15-6b49dc6f4efa">Picture</a> property.


## -enum-fields




### -field IPSM_AutoSize

The control auto sizes to fit the picture.


### -field IPSM_CenterImage

The picture is centered within the control.


### -field IPSM_Normal

The picture appears at its regular size within the control.


### -field IPSM_StretchImage

 The picture is stretched within the control.


## -see-also




<a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a>
 

 

