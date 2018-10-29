---
UID: NF:mfcaptureengine.IMFCaptureRecordSink.SetRotation
title: IMFCaptureRecordSink::SetRotation
author: windows-sdk-content
description: Rotates the recorded video stream.
old-location: mf\imfcapturerecordsink_setrotation.htm
tech.root: medfound
ms.assetid: 3C451FF9-F5CD-48C6-A7FE-88BD3E82DA83
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IMFCaptureRecordSink interface [Media Foundation],SetRotation method, IMFCaptureRecordSink.SetRotation, IMFCaptureRecordSink::SetRotation, SetRotation, SetRotation method [Media Foundation], SetRotation method [Media Foundation],IMFCaptureRecordSink interface, mf.imfcapturerecordsink_setrotation, mfcaptureengine/IMFCaptureRecordSink::SetRotation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfcaptureengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - COM
api_location:
 - mfcaptureengine.h
api_name:
 - IMFCaptureRecordSink.SetRotation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFCaptureRecordSink::SetRotation


## -description


Rotates the recorded video stream.


## -parameters




### -param dwStreamIndex [in]

The zero-based index of the stream to rotate. You must specify a video stream.


### -param dwRotationValue [in]

The amount to rotate the video, in degrees. Valid values are 0, 90, 180, and 270. The value zero restores the video to its original orientation.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/AEF5923D-C4ED-4BEA-A969-163ED837A5BD">IMFCaptureRecordSink</a>
 

 

