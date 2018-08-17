---
UID: NF:spatialaudioclient.ISpatialAudioObjectRenderStreamBase.GetAvailableDynamicObjectCount
title: ISpatialAudioObjectRenderStreamBase::GetAvailableDynamicObjectCount
author: windows-sdk-content
description: Gets the number of dynamic spatial audio objects that are currently available.
old-location: coreaudio\ispatialaudioobjectrenderstream_getavailabledynamicobjectcount.htm
old-project: CoreAudio
ms.assetid: 5E17B53A-B999-4B08-9DFB-96D55E7F9CF7
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: GetAvailableDynamicObjectCount, GetAvailableDynamicObjectCount method [Core Audio], GetAvailableDynamicObjectCount method [Core Audio],ISpatialAudioObjectRenderStreamBase interface, ISpatialAudioObjectRenderStreamBase interface [Core Audio],GetAvailableDynamicObjectCount method, ISpatialAudioObjectRenderStreamBase.GetAvailableDynamicObjectCount, ISpatialAudioObjectRenderStreamBase::GetAvailableDynamicObjectCount, coreaudio.ispatialaudioobjectrenderstream_getavailabledynamicobjectcount, spatialaudioclient/ISpatialAudioObjectRenderStreamBase::GetAvailableDynamicObjectCount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: spatialaudioclient.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: AudioObjectType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - spatialaudioclient.h
api_name:
 - ISpatialAudioObjectRenderStreamBase.GetAvailableDynamicObjectCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ISpatialAudioObjectRenderStreamBase::GetAvailableDynamicObjectCount


## -description


Gets the number of dynamic spatial audio objects that are currently available.


## -parameters




### -param value [out]

The number of dynamic spatial audio objects that are currently available.


## -returns



If the method succeeds, it returns S_OK.




## -remarks



A dynamic <a href="https://msdn.microsoft.com/EE83AF5F-4342-4CF2-81A7-1123F8DAFA6F">ISpatialAudioObject</a> is one that was activated by setting the <i>type</i> parameter to the  <a href="https://msdn.microsoft.com/1B99E7FB-0796-4902-9B00-470FD08F8AFA">ActivateSpatialAudioObject</a> method to <b>AudioObjectType_Dynamic</b>. The system has a limit of the maximum number of dynamic spatial audio objects that can be activated at one time. Call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> on an <b>ISpatialAudioObject</b>  when it is no longer being used to free up the resource to create new dynamic spatial audio objects.




## -see-also




<a href="https://msdn.microsoft.com/B4D10CC6-62BF-4D20-910F-E39DF812010D">ISpatialAudioObjectRenderStream</a>



<a href="coreaudio.ispatialaudioobjectrenderstreambase">ISpatialAudioObjectRenderStreamBase</a>
 

 

