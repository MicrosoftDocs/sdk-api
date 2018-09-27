---
UID: NF:mfspatialaudio.IMFSpatialAudioObjectBuffer.GetType
title: IMFSpatialAudioObjectBuffer::GetType
author: windows-sdk-content
description: Gets the type of the spatial audio object represented by the buffer. If SetType has not been called previously, this method returns the default value of AudioObjectType_None.
old-location: mf\imfspatialaudioobjectbuffer_gettype.htm
tech.root: medfound
ms.assetid: CF0285D2-E56B-44A5-B7E0-3227213D9523
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: GetType, GetType method [Media Foundation], GetType method [Media Foundation],IMFSpatialAudioObjectBuffer interface, IMFSpatialAudioObjectBuffer interface [Media Foundation],GetType method, IMFSpatialAudioObjectBuffer.GetType, IMFSpatialAudioObjectBuffer::GetType, mf.imfspatialaudioobjectbuffer_gettype, mfspatialaudio/IMFSpatialAudioObjectBuffer::GetType
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Mfobjects.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfobjects.lib
 - mfobjects.dll
api_name:
 - IMFSpatialAudioObjectBuffer.GetType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSpatialAudioObjectBuffer::GetType


## -description


Gets the type of the spatial audio object represented by the buffer. If <a href="https://msdn.microsoft.com/3D21D093-FDCE-4ECA-B8B2-56D6E5D5D9C6">SetType</a> has not been called previously, this method returns the default value of <b>AudioObjectType_None</b>.


## -parameters




### -param pType [out]

A pointer to an <a href="https://msdn.microsoft.com/DFFE770F-41C0-4048-A38F-FB96353E9216">AudioObjectType</a> variable where the audio object type will be stored.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The supplied pointer is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/61E9BC6A-2120-4874-9053-E1D232DF1CCA">IMFSpatialAudioObjectBuffer</a>
 

 

