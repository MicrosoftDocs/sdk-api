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

# _DD_CREATEMOCOMPDATA structure


## -description


The DD_CREATEMOCOMPDATA structure contains the data required to begin using motion compensation. 


## -struct-fields




### -field lpDD

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550595">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.


### -field lpMoComp

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551663">DD_MOTIONCOMP_LOCAL</a> structure that contains a description of the motion compensation object.


### -field lpGuid

Points to a GUID that describes the motion compensation process being used.


### -field dwUncompWidth

Specifies the width in pixels of the uncompressed output frame. 


### -field dwUncompHeight

Specifies the height in pixels of the uncompressed output frame. 


### -field ddUncompPixelFormat

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550274">DDPIXELFORMAT</a> structure that contains the format of the uncompressed output frame. 


### -field lpData

Points to an optional data buffer that contains any optional information required by the GUID given in <b>lpGuid</b>. This buffer cannot contain any embedded pointers.


### -field dwDataSize

Indicates the size in bytes of the data buffer contained in <b>lpData</b>. 


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/9413108b-f9b5-4d1c-83a9-b663a9f444bf">DdMoCompCreate</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


## -see-also




<a href="https://msdn.microsoft.com/9413108b-f9b5-4d1c-83a9-b663a9f444bf">DdMoCompCreate</a>
 

 

