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

# _VMR9PresentationInfo structure


## -description



The <code>VMR9PresentationInfo</code> structure is used with the VMR-9 in the <a href="https://msdn.microsoft.com/1c642958-88df-48b2-8eb1-0d032af71f71">IVMRImagePresenter9::PresentImage</a> method.




## -struct-fields




### -field dwFlags

Contains a bitwise combintation of flags from the <a href="https://msdn.microsoft.com/97db420f-a6a5-4c87-9c7f-9733a1ce2b46">VMR9PresentationFlags</a> enumeration type. These flags describe the status of the video sample with respect to its presentation time.


### -field lpSurf

Pointer to the DirectDraw surface that contains the video frame.


### -field rtStart

Specifies the start time for the video frame.


### -field rtEnd

Specifies the end time for the video frame


### -field szAspectRatio

Specifies the aspect ratio of the video, as a <b>SIZE</b> structure.


### -field rcSrc

Specifies the source rectangle.


### -field rcDst

Specifies the destination rectangle.


### -field dwReserved1

Reserved.


### -field dwReserved2

Reserved.


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

