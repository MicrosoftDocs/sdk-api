---
UID: NE:mfidl._MFMEDIASOURCE_CHARACTERISTICS
title: "_MFMEDIASOURCE_CHARACTERISTICS"
author: windows-sdk-content
description: Defines the characteristics of a media source.
old-location: mf\mfmediasource_characteristics.htm
old-project: medfound
ms.assetid: 115f4a6b-99c2-436e-9483-c44003e61a7d
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: 115f4a6b-99c2-436e-9483-c44003e61a7d, MFMEDIASOURCE_CAN_PAUSE, MFMEDIASOURCE_CAN_SEEK, MFMEDIASOURCE_CAN_SKIPBACKWARD, MFMEDIASOURCE_CAN_SKIPFORWARD, MFMEDIASOURCE_CHARACTERISTICS, MFMEDIASOURCE_CHARACTERISTICS enumeration [Media Foundation], MFMEDIASOURCE_DOES_NOT_USE_NETWORK, MFMEDIASOURCE_HAS_MULTIPLE_PRESENTATIONS, MFMEDIASOURCE_HAS_SLOW_SEEK, MFMEDIASOURCE_IS_LIVE, _MFMEDIASOURCE_CHARACTERISTICS, mf.mfmediasource_characteristics, mfidl/MFMEDIASOURCE_CAN_PAUSE, mfidl/MFMEDIASOURCE_CAN_SEEK, mfidl/MFMEDIASOURCE_CAN_SKIPBACKWARD, mfidl/MFMEDIASOURCE_CAN_SKIPFORWARD, mfidl/MFMEDIASOURCE_CHARACTERISTICS, mfidl/MFMEDIASOURCE_DOES_NOT_USE_NETWORK, mfidl/MFMEDIASOURCE_HAS_MULTIPLE_PRESENTATIONS, mfidl/MFMEDIASOURCE_HAS_SLOW_SEEK, mfidl/MFMEDIASOURCE_IS_LIVE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MFMEDIASOURCE_CHARACTERISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFMEDIASOURCE_CHARACTERISTICS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MFMEDIASOURCE_CHARACTERISTICS enumeration


## -description


Defines the characteristics of a media source. These flags are retrieved by the <a href="https://msdn.microsoft.com/cb5d54cd-58a3-4903-b22e-8207f90dbbc0">IMFMediaSource::GetCharacteristics</a> method.


## -enum-fields




### -field MFMEDIASOURCE_IS_LIVE


            This flag indicates a data source that runs constantly, such as a live presentation. If the source is stopped and then restarted, there will be a gap in the content.
          


### -field MFMEDIASOURCE_CAN_SEEK


            The media source supports seeking.
          


### -field MFMEDIASOURCE_CAN_PAUSE


            The source can pause.
          


### -field MFMEDIASOURCE_HAS_SLOW_SEEK


            The media source downloads content. It might take a long time to seek to parts of the content that have not been downloaded.
          


### -field MFMEDIASOURCE_HAS_MULTIPLE_PRESENTATIONS

The media source delivers a playlist, which might contain more than one entry. After the first playlist entry has completed, the media source signals the start of each new playlist entry by sending an <a href="https://msdn.microsoft.com/c669b2c9-5ece-4045-b691-8a71bbf491e1">MENewPresentation</a> event. The event contains a presentation descriptor for the entry.

<div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>

### -field MFMEDIASOURCE_CAN_SKIPFORWARD

The media source can skip forward in the playlist. Applies only if the MFMEDIASOURCE_HAS_MULTIPLE_PRESENTATIONS flag is present. 

<div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>

### -field MFMEDIASOURCE_CAN_SKIPBACKWARD

The media source can skip backward in the playlist.

<div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>

### -field MFMEDIASOURCE_DOES_NOT_USE_NETWORK

The media source is not currently
    using the network to receive the content.  Networking hardware
    may enter a power saving state when this bit is set.

<div class="alert"><b>Note</b>  Requires Windows 8 or later.</div>
<div> </div>

## -remarks



To skip forward or backward in a playlist, call <a href="https://msdn.microsoft.com/0a5abafe-1525-4bda-946c-05a6145e57ee">IMFMediaSource::Start</a> or <a href="https://msdn.microsoft.com/1bdec0c0-b042-4e5e-a72b-b15942750ced">IMFMediaSession::Start</a> with the <b>MF_TIME_FORMAT_ENTRY_RELATIVE</b> time-format GUID. This capability applies only when the <b>MFMEDIASOURCE_HAS_MULTIPLE_PRESENTATIONS</b> flag is present.




## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

