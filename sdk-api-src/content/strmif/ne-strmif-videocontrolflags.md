---
UID: NE:strmif.tagVideoControlFlags
title: VideoControlFlags (strmif.h)
description: Specifies the video mode of operation for a video device.helpviewer_keywords: ["VideoControlFlag_ExternalTriggerEnable","VideoControlFlag_FlipHorizontal","VideoControlFlag_FlipVertical","VideoControlFlag_Trigger","VideoControlFlags","VideoControlFlags enumeration [DirectShow]","VideoControlFlagsEnumeration","dshow.videocontrolflags","strmif/VideoControlFlag_ExternalTriggerEnable","strmif/VideoControlFlag_FlipHorizontal","strmif/VideoControlFlag_FlipVertical","strmif/VideoControlFlag_Trigger","strmif/VideoControlFlags"]
old-location: dshow\videocontrolflags.htm
tech.root: DirectShow
ms.assetid: 9d7feb46-fb07-46d8-a9a5-511578873cf3
ms.date: 12/05/2018
ms.keywords: VideoControlFlag_ExternalTriggerEnable, VideoControlFlag_FlipHorizontal, VideoControlFlag_FlipVertical, VideoControlFlag_Trigger, VideoControlFlags, VideoControlFlags enumeration [DirectShow], VideoControlFlagsEnumeration, dshow.videocontrolflags, strmif/VideoControlFlag_ExternalTriggerEnable, strmif/VideoControlFlag_FlipHorizontal, strmif/VideoControlFlag_FlipVertical, strmif/VideoControlFlag_Trigger, strmif/VideoControlFlags
f1_keywords:
- strmif/VideoControlFlags
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- strmif.h
api_name:
- VideoControlFlags
targetos: Windows
req.typenames: VideoControlFlags
req.redist: 
ms.custom: 19H1
---

# VideoControlFlags enumeration


## -description



Specifies the video mode of operation for a video device.




## -enum-fields




### -field VideoControlFlag_FlipHorizontal

Specifies that the picture is flipped horizontally.


### -field VideoControlFlag_FlipVertical

Specifies that the picture is flipped vertically.


### -field VideoControlFlag_ExternalTriggerEnable

Sets up a stream to capture a trigger from an external source, for example, a push button on a camera. Buffers can be queued to the driver but will not be passed up from the WDM capture driver (for compression, display, or writing to a file) until the external event happens. See Remarks.


### -field VideoControlFlag_Trigger

In software, simulates an external trigger when the stream has the VideoControlFlag_ExternalTriggerEnable flag set.


## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamvideocontrol">IAMVideoControl</a> interface uses this enumerated data type.

Multiple capture buffers are queued to a capture driver and are filled at a fixed rate once the stream is put into the "run" state. If the VideoControlFlag_ExternalTriggerEnable flag is set, a filled buffer is not passed up from the WDM capture driver for compression, display, or writing to a file until the external event happens.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamvideocontrol">IAMVideoControl</a>
 

 

