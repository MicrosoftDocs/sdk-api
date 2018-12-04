---
UID: NF:vfw.ICDrawStartPlay
title: ICDrawStartPlay macro
author: windows-sdk-content
description: The ICDrawStartPlay macro provides the start and end times of a play operation to a rendering driver. You can use this macro or explicitly call the ICM_DRAW_START_PLAY message.
old-location: multimedia\icdrawstartplay.htm
tech.root: Multimedia
ms.assetid: 74957f08-2912-4e5e-af45-7dc66b405bc2
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: ICDrawStartPlay, ICDrawStartPlay macro [Windows Multimedia], _win32_ICDrawStartPlay, multimedia.icdrawstartplay, vfw/ICDrawStartPlay
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - ICDrawStartPlay
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICDrawStartPlay macro


## -description



The <b>ICDrawStartPlay</b> macro provides the start and end times of a play operation to a rendering driver. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/27c4c06e-6510-43dc-a754-fe44144796f5">ICM_DRAW_START_PLAY</a> message.




## -parameters




### -param hic

Handle to a driver. 


### -param lFrom

Start time. 


### -param lTo

End time. 


## -remarks



This message precedes any frame data sent to the rendering driver.

Units for <i>lFrom</i> and <i>lTo</i> are specified with the <a href="https://msdn.microsoft.com/e5ecd7dd-376b-422c-bbb8-4e7c41e3cac8">ICM_DRAW_BEGIN</a> message. For video data this is normally a frame number. For more information about the playback rate, see the <b>dwRate</b> and <b>dwScale</b> members of the <a href="https://msdn.microsoft.com/1ec2309c-7ea8-423e-aee3-5e0c650f0b3d">ICDRAWBEGIN</a> structure.

If the end time is less than the start time, the playback direction is reversed.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

