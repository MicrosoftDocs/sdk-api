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

# DisplaySizeList enumeration


## -description



This topic applies to Windows XP or later.
        



The <b>DisplaySizeList</b> enumeration defines the possible sizes at which the video rectangle may be rendered.


## -enum-fields




### -field dslDefaultSize

Display the video rectangle at the native size.


### -field dslSourceSize

Same as <b>dslDefaultSize</b>.


### -field dslHalfSourceSize

Display the video rectangle by shrinking the width and height by half.


### -field dslDoubleSourceSize

Display the video rectangle by stretching the width and height to twice their native size.


### -field dslFullScreen

Display the video rectangle by stretching the width and height to fill the entire screen as much as possible while maintaining the original aspect ratio.


### -field dslHalfScreen

Display the video rectangle by stretching the width and height as much as possible to fill half (50%) of the screen while maintaining the original aspect ratio.


### -field dslQuarterScreen

Display the video rectangle by stretching the width and height as much as possible to fill one quarter (25%) of the screen while maintaining the original aspect ratio.


### -field dslSixteenthScreen

Display the video rectangle by stretching the width and height as much as possible to fill one sixteenth (6.25%) of the screen while maintaining the original aspect ratio.


## -see-also




<a href="https://msdn.microsoft.com/f3d5ed73-4781-46fb-8df4-a7dc339b755c">IMSVidCtl::get_DisplaySize</a>



<a href="https://msdn.microsoft.com/1771e66b-e5f3-44f5-a489-e57baaf5cf25">IMSVidCtl::put_DisplaySize</a>
 

 

