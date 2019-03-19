---
UID: NF:spatialaudioclient.ISpatialAudioObjectBase.IsActive
title: ISpatialAudioObjectBase::IsActive (spatialaudioclient.h)
author: windows-sdk-content
description: Gets a boolean value indicating whether the ISpatialAudioObject is valid.
old-location: coreaudio\ispatialaudioobject_isactive.htm
tech.root: CoreAudio
ms.assetid: 3339E021-4AC3-43CB-9306-C8D58541CA5F
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISpatialAudioObjectBase interface [Core Audio],IsActive method, ISpatialAudioObjectBase.IsActive, ISpatialAudioObjectBase::IsActive, IsActive, IsActive method [Core Audio], IsActive method [Core Audio],ISpatialAudioObjectBase interface, coreaudio.ispatialaudioobject_isactive, spatialaudioclient/ISpatialAudioObjectBase::IsActive
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
 - ISpatialAudioObjectBase.IsActive
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpatialAudioObjectBase::IsActive


## -description


Gets a boolean value indicating whether the <a href="https://msdn.microsoft.com/EE83AF5F-4342-4CF2-81A7-1123F8DAFA6F">ISpatialAudioObject</a> is valid. 


## -parameters




### -param isActive [out]

<b>TRUE</b> if the audio object is currently valid; otherwise, <b>FALSE</b>.


## -returns



If the method succeeds, it returns S_OK.




## -remarks



If this value is false, you should call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> to make the audio object resource available in the future.

<b>IsActive</b> will be set to false after <a href="https://msdn.microsoft.com/17294E5D-04D7-43B9-AD41-392344309308">SetEndOfStream</a> is called implicitly or explicitly. <b>SetEndOfStream</b> is called implicitly by the system if <a href="https://msdn.microsoft.com/CD777E2D-4CA0-4C2D-A475-22BF770DD59D">GetBuffer</a> is not called within an audio processing pass (between calls to <a href="https://msdn.microsoft.com/9D858556-2EBE-4DF6-878B-BE0E12079248">ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects</a> and <a href="https://msdn.microsoft.com/111DB695-66F6-45DD-B3B6-1DFB0D5D29FC">ISpatialAudioObjectRenderStream::EndUpdatingAudioObjects</a>).

The rendering engine will also deactivate the audio object, setting <b>IsActive</b> to false, when audio object resources become unavailable. In this case, a notification is sent via <a href="https://msdn.microsoft.com/3729D985-9040-43AD-A8B0-045509FE2F20">ISpatialAudioObjectRenderStreamNotify</a> before the object is deactivated. The value returned in the <i>availableDynamicObjectCount</i> parameter to <a href="https://msdn.microsoft.com/9D858556-2EBE-4DF6-878B-BE0E12079248">ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects</a> indicates how many objects will be processed for each pass.




## -see-also




<a href="https://msdn.microsoft.com/EE83AF5F-4342-4CF2-81A7-1123F8DAFA6F">ISpatialAudioObject</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt829727(v=VS.85).aspx">ISpatialAudioObjectBase</a>
 

 

