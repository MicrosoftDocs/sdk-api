---
UID: NF:spatialaudioclient.ISpatialAudioClient.GetNativeStaticObjectTypeMask
title: ISpatialAudioClient::GetNativeStaticObjectTypeMask
author: windows-sdk-content
description: Gets a channel mask which represents the subset of static speaker bed channels native to current rendering engine.
old-location: coreaudio\ispatialaudioclient_getnativestaticobjecttypemask.htm
tech.root: CoreAudio
ms.assetid: 29963682-AD45-4CEC-81A0-4B834505F9D5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetNativeStaticObjectTypeMask, GetNativeStaticObjectTypeMask method [Core Audio], GetNativeStaticObjectTypeMask method [Core Audio],ISpatialAudioClient interface, ISpatialAudioClient interface [Core Audio],GetNativeStaticObjectTypeMask method, ISpatialAudioClient.GetNativeStaticObjectTypeMask, ISpatialAudioClient::GetNativeStaticObjectTypeMask, coreaudio.ispatialaudioclient_getnativestaticobjecttypemask, spatialaudioclient/ISpatialAudioClient::GetNativeStaticObjectTypeMask
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
 - ISpatialAudioClient.GetNativeStaticObjectTypeMask
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpatialAudioClient::GetNativeStaticObjectTypeMask


## -description


Gets a  channel mask which represents the subset of static speaker bed channels native to current rendering engine.


## -parameters




### -param mask [out]

A bitwise combination of values from the <a href="https://msdn.microsoft.com/DFFE770F-41C0-4048-A38F-FB96353E9216">AudioObjectType</a> enumeration indicating a subset of static speaker channels. The values returned will only include the static channel values and will not include <b>AudioObjectType_Dynamic</b>.


## -returns



If the method succeeds, it returns S_OK.




## -see-also




<a href="https://msdn.microsoft.com/950778D4-79FE-4222-951F-5A456A633124">ISpatialAudioClient</a>
 

 

