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

# _WTS_CLIENT_DISPLAY structure


## -description


Contains information about the display of a Remote Desktop Connection (RDC) client.


## -struct-fields




### -field HorizontalResolution

Horizontal dimension, in pixels, of the client's display.


### -field VerticalResolution

Vertical dimension, in pixels, of the client's display.


### -field ColorDepth

Color depth of the client's display. This member can be one of the following values.



#### 1

4 bits per pixel.



#### 2

8 bits per pixel.



#### 4

16 bits per pixel.



#### 8

A 3-byte RGB values for a maximum of 2^24 colors.



#### 16

15 bits per pixel.



#### 24

24 bits per pixel.



#### 32

32 bits per pixel.


## -see-also




<a href="https://msdn.microsoft.com/d52345a4-0408-4ea9-ba71-349910143752">WTSQuerySessionInformation</a>
 

 

