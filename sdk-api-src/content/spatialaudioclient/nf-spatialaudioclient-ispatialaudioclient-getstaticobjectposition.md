---
UID: NF:spatialaudioclient.ISpatialAudioClient.GetStaticObjectPosition
title: ISpatialAudioClient::GetStaticObjectPosition
author: windows-sdk-content
description: Gets the position in 3D space of the specified static spatial audio channel.
old-location: coreaudio\ispatialaudioclient_getstaticobjectposition.htm
tech.root: CoreAudio
ms.assetid: F8CD558A-994D-46E0-98A0-1D7AD3B919C0
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: GetStaticObjectPosition, GetStaticObjectPosition method [Core Audio], GetStaticObjectPosition method [Core Audio],ISpatialAudioClient interface, ISpatialAudioClient interface [Core Audio],GetStaticObjectPosition method, ISpatialAudioClient.GetStaticObjectPosition, ISpatialAudioClient::GetStaticObjectPosition, coreaudio.ispatialaudioclient_getstaticobjectposition, spatialaudioclient/ISpatialAudioClient::GetStaticObjectPosition
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: spatialaudioclient.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - spatialaudioclient.h
api_name:
 - ISpatialAudioClient.GetStaticObjectPosition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpatialAudioClient::GetStaticObjectPosition


## -description


Gets the position in 3D space of the specified static spatial audio channel. 


## -parameters




### -param type [in]

A value indicating the static spatial audio channel for which the position is being queried. This method will return E_INVALIDARG  if the value does not represent a static channel, including <b>AudioObjectType_Dynamic</b> and <b>AudioObjectType_None</b>.


### -param x [out]

The x coordinate of the static audio channel, in meters, relative to the listener. Positive values are to the right of the listener and negative values are to the left.


### -param y [out]

The y coordinate of the static audio channel, in meters, relative to the listener. Positive values are above the listener and negative values are below.


### -param z [out]

The z coordinate of the static audio channel, in meters, relative to the listener. Positive values are behind the listener and negative values are in front.


## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The supplied  <a href="https://msdn.microsoft.com/DFFE770F-41C0-4048-A38F-FB96353E9216">AudioObjectType</a> value does not represent a static channel.

</td>
</tr>
</table>
 




## -remarks



 Position values use a right-handed Cartesian coordinate system, where each unit represents 1 meter. The coordinate system is relative to the listener where the origin (x=0.0, y=0.0, z=0.0) represents the center point between the listener's ears.




## -see-also




<a href="https://msdn.microsoft.com/950778D4-79FE-4222-951F-5A456A633124">ISpatialAudioClient</a>
 

 

