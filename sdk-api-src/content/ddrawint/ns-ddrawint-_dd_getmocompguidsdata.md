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

# _DD_GETMOCOMPGUIDSDATA structure


## -description


The DD_GETMOCOMPGUIDSDATA structure contains the motion compensation GUID information. 


## -struct-fields




### -field lpDD

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550595">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.


### -field dwNumGuids

Indicates the number of motion compensation GUIDs in <b>lpGuids</b>. 


### -field lpGuids

Points to a list of GUIDs that describe the motion compensation processes being used. If <b>lpGuids</b> is <b>NULL</b>, the driver should set <b>dwNumGuids</b> to the number of GUIDs that it supports. Otherwise, it should fill <b>lpGuids</b> with the GUIDs that it supports and set the number in <b>dwNumGuids</b>.


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/22c6a3f2-4a27-4a4b-a021-8f2be04e4f87">DdMoCompGetGuids</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


## -see-also




<a href="https://msdn.microsoft.com/22c6a3f2-4a27-4a4b-a021-8f2be04e4f87">DdMoCompGetGuids</a>
 

 

