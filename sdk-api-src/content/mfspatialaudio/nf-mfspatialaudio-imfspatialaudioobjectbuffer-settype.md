---
UID: NF:mfspatialaudio.IMFSpatialAudioObjectBuffer.SetType
title: IMFSpatialAudioObjectBuffer::SetType
author: windows-sdk-content
description: Sets the type of the spatial audio object represented by the buffer.
old-location: mf\imfspatialaudioobjectbuffer_settype.htm
old-project: medfound
ms.assetid: 3D21D093-FDCE-4ECA-B8B2-56D6E5D5D9C6
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IMFSpatialAudioObjectBuffer interface [Media Foundation],SetType method, IMFSpatialAudioObjectBuffer.SetType, IMFSpatialAudioObjectBuffer::SetType, SetType, SetType method [Media Foundation], SetType method [Media Foundation],IMFSpatialAudioObjectBuffer interface, mf.imfspatialaudioobjectbuffer_settype, mfspatialaudio/IMFSpatialAudioObjectBuffer::SetType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfspatialaudio.h
req.include-header: Mfobjects.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: DEVICE_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfobjects.lib
 - mfobjects.dll
api_name:
 - IMFSpatialAudioObjectBuffer.SetType
product: Windows
targetos: Windows
req.lib: Mfobjects.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSpatialAudioObjectBuffer::SetType


## -description


Sets the type of the spatial audio object represented by the buffer.


## -parameters




### -param type

A value from the <a href="https://msdn.microsoft.com/DFFE770F-41C0-4048-A38F-FB96353E9216">AudioObjectType</a> enumeration specifying the type of audio object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A spatial audio object can be of type <b>AudioObjectType_Dynamic</b>, which means that it can change position and orientation in 3D space over time, or it can have a value such as <b>AudioObjectType_FrontLeft</b> which represents the static position of a real or virtual speaker that does not change position over time.




## -see-also




<a href="https://msdn.microsoft.com/61E9BC6A-2120-4874-9053-E1D232DF1CCA">IMFSpatialAudioObjectBuffer</a>
 

 

