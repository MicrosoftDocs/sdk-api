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

# _COPYFILE2_COPY_PHASE enumeration


## -description


Indicates the phase of a copy at the time of an error. This is used in the 
    <b>Error</b> structure embedded in the 
    <a href="https://msdn.microsoft.com/ab841bee-90a0-4beb-99d3-764e608c3872">COPYFILE2_MESSAGE</a> structure.


## -enum-fields




### -field COPYFILE2_PHASE_NONE

The copy had not yet started processing.


### -field COPYFILE2_PHASE_PREPARE_SOURCE

The source was being prepared including opening a handle to the source. This phase happens once per stream 
      copy operation.


### -field COPYFILE2_PHASE_PREPARE_DEST

The destination was being prepared including opening a handle to the destination. This phase happens once 
      per stream copy operation.


### -field COPYFILE2_PHASE_READ_SOURCE

The source file was being read. This phase happens one or more times per stream copy operation.


### -field COPYFILE2_PHASE_WRITE_DESTINATION

The destination file was being written. This phase happens one or more times per stream copy 
      operation.


### -field COPYFILE2_PHASE_SERVER_COPY

Both the source and destination were on the same remote server and the copy was being processed remotely. 
      This phase happens once per stream copy operation.


### -field COPYFILE2_PHASE_NAMEGRAFT_COPY

The copy operation was processing symbolic links and/or reparse points. This phase happens once per file 
      copy operation.


### -field COPYFILE2_PHASE_MAX

One greater than the maximum value. Valid values for this enumeration will be less than this value.


## -remarks



To compile an application that uses this enumeration, define the <b>_WIN32_WINNT</b> 
    macro as 0x0601 or later. For more information, see 
    <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/ab841bee-90a0-4beb-99d3-764e608c3872">COPYFILE2_MESSAGE</a>



<a href="https://msdn.microsoft.com/aa2df686-4b61-4d90-ba0b-c78c5a0d2d59">CopyFile2</a>



<a href="https://msdn.microsoft.com/14b1cfff-5e47-4309-8e62-fb5c8da9ce97">File Management Enumerations</a>
 

 

