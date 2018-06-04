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

# WMT_RIGHTS enumeration


## -description



      
        The <b>WMT_RIGHTS</b> enumeration type defines the rights that may be specified in a DRM license.


## -enum-fields




### -field WMT_RIGHT_PLAYBACK

Specifies the right to play content without restriction.


### -field WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE

Specifies the right to copy content to a device not compliant with the <a href="wmformat_glossary.htm">Secure Digital Music Initiative (SDMI)</a>.


### -field WMT_RIGHT_COPY_TO_CD

Specifies the right to copy content to a CD.


### -field WMT_RIGHT_COPY_TO_SDMI_DEVICE

Specifies the right to copy content to a device compliant with the Secure Digital Music Initiative (SDMI).


### -field WMT_RIGHT_ONE_TIME

Specifies the right to play content one time only.


### -field WMT_RIGHT_SAVE_STREAM_PROTECTED

Specifies the right to save content from a server.


### -field WMT_RIGHT_COPY

Specifies the right to copy content. Windows Media DRM 10 regulates the devices to which the content can be copied by using output protection levels (OPLs).


### -field WMT_RIGHT_COLLABORATIVE_PLAY

Specifies the right to play content as part of an online scenario where multiple participants can contribute songs from their collection to a shared playlist.


### -field WMT_RIGHT_SDMI_TRIGGER

Reserved for future use. Do not use.


### -field WMT_RIGHT_SDMI_NOMORECOPIES

Reserved for future use. Do not use.


## -remarks



These values are bit flags, so one or more can be set by combining them with the bitwise <b>OR</b> operator.

When using Windows Media DRM 10, <b>WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE</b>, <b>WMT_RIGHT_COPY_TO_SDMI_DEVICE</b>, and <b>WMT_RIGHT_COPY_TO_CD</b> are superseded by <b>WMT_RIGHT_COPY</b>. Limitations on the devices to which the content may be copied are specified by using output protection levels (OPLs).




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545452">Enumeration Types</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538799">WAVEFORMATEX</a>
 

 

