---
UID: NF:mfmediaengine.IMFTimedTextTrack.GetExtendedErrorCode
title: IMFTimedTextTrack::GetExtendedErrorCode
author: windows-sdk-content
description: Gets the extended error code for the latest error associated with the track.
old-location: mf\imftimedtexttrack_getextendederrorcode.htm
tech.root: medfound
ms.assetid: 61119103-B6F6-414B-AA7E-55DC889A5C28
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetExtendedErrorCode, GetExtendedErrorCode method [Media Foundation], GetExtendedErrorCode method [Media Foundation],IMFTimedTextTrack interface, IMFTimedTextTrack interface [Media Foundation],GetExtendedErrorCode method, IMFTimedTextTrack.GetExtendedErrorCode, IMFTimedTextTrack::GetExtendedErrorCode, mf.imftimedtexttrack_getextendederrorcode, mfmediaengine/IMFTimedTextTrack::GetExtendedErrorCode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
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
req.lib: Mfmediaengine.lib
req.dll: Mfmediaengine.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.dll
api_name:
 - IMFTimedTextTrack.GetExtendedErrorCode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTimedTextTrack::GetExtendedErrorCode


## -description


Gets the extended error code for the latest error associated with the track.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

The extended error code for the latest error associated with the track.




## -remarks



If the most recent error was associated with a track, this value will be the same <a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a> as returned by the <a href="https://msdn.microsoft.com/3658EE26-497D-4D33-BE68-572BCE1B28B1">IMFTimedTextNotify::Error</a> method.




## -see-also




<a href="https://msdn.microsoft.com/55232D19-F3D0-42C7-8B24-C2A7768B2C7E">IMFTimedTextTrack</a>
 

 

