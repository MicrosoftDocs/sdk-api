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

# MCI_DGV_STATUS_PARMSW structure


## -description



The <b>MCI_DGV_STATUS_PARMS</b> structure contains parameters for the <a href="https://msdn.microsoft.com/d1c3dff9-c66f-4525-aac1-4a15b43083e7">MCI_STATUS</a> command for digital-video devices.




## -struct-fields




### -field dwCallback

The low-order word specifies a window handle used for the MCI_NOTIFY flag.


### -field dwReturn

Buffer for return information.


### -field dwItem

Identifies capability being queried.


### -field dwTrack

Length or number of tracks.


### -field lpstrDrive

Specifies the approximate amount of disk space that can be obtained by the <a href="https://msdn.microsoft.com/01f0a377-0179-4b05-a642-af152a7a12ae">MCI_RESERVE</a> command.


### -field dwReference

Specifies the approximate location of the nearest previous intraframe-encoded image.


## -remarks



When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a> function to validate the members.




## -see-also




<a href="https://msdn.microsoft.com/b414dffb-3701-4dfd-aa8c-cd8e8918027d">MCI</a>



<a href="https://msdn.microsoft.com/e86740e5-633e-465d-94ef-8065a8c05b31">MCI Structures</a>



<a href="https://msdn.microsoft.com/01f0a377-0179-4b05-a642-af152a7a12ae">MCI_RESERVE</a>



<a href="https://msdn.microsoft.com/d1c3dff9-c66f-4525-aac1-4a15b43083e7">MCI_STATUS</a>



<a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a>
 

 

