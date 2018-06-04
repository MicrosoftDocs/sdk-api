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

# MCI_DGV_COPY_PARMS structure


## -description



The <b>MCI_DGV_COPY_PARMS</b> structure contains parameters for the <a href="https://msdn.microsoft.com/41807920-3312-4cdb-82e6-6ab4b9b35162">MCI_COPY</a> command for digital-video devices.




## -struct-fields




### -field dwCallback


            The low-order word specifies a window handle used for the MCI_NOTIFY flag.
          


### -field dwFrom


            Starting position for copy.
          


### -field dwTo


            Ending position for copy.
          


### -field ptOffset

 


### -field ptExtent

 


### -field rc

Rectangle describing area to be copied.   Be aware that <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structures are handled differently in MCI than in other parts of Windows; in MCI, <b>rc.right</b> contains the width of the rectangle and <b>rc.bottom</b> contains its height.


### -field dwAudioStream


            Audio stream.
          


### -field dwVideoStream


            Video stream.
          


## -remarks



When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a> function to validate the members.




## -see-also




<a href="https://msdn.microsoft.com/b414dffb-3701-4dfd-aa8c-cd8e8918027d">MCI</a>



<a href="https://msdn.microsoft.com/e86740e5-633e-465d-94ef-8065a8c05b31">MCI Structures</a>



<a href="https://msdn.microsoft.com/41807920-3312-4cdb-82e6-6ab4b9b35162">MCI_COPY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>



<a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a>
 

 

