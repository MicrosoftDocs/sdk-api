---
UID: NF:spatialaudioclient.ISpatialAudioObjectBase.GetAudioObjectType
title: ISpatialAudioObjectBase::GetAudioObjectType
author: windows-sdk-content
description: Gets a value specifying the type of audio object that is represented by the ISpatialAudioObject.
old-location: coreaudio\ispatialaudioobject_getaudioobjecttype.htm
old-project: CoreAudio
ms.assetid: C4FB5E8B-C80A-4B4B-9162-95B463543061
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetAudioObjectType, GetAudioObjectType method [Core Audio], GetAudioObjectType method [Core Audio],ISpatialAudioObjectBase interface, ISpatialAudioObjectBase interface [Core Audio],GetAudioObjectType method, ISpatialAudioObjectBase.GetAudioObjectType, ISpatialAudioObjectBase::GetAudioObjectType, coreaudio.ispatialaudioobject_getaudioobjecttype, spatialaudioclient/ISpatialAudioObjectBase::GetAudioObjectType
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
 - ISpatialAudioObjectBase.GetAudioObjectType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ISpatialAudioObjectBase::GetAudioObjectType


## -description


Gets a value specifying the type of audio object that is represented by the <a href="https://msdn.microsoft.com/EE83AF5F-4342-4CF2-81A7-1123F8DAFA6F">ISpatialAudioObject</a>. This value indicates if the object is dynamic or static. If the object is static, one and only one of the static audio channel values to which the object is assigned is returned.


## -parameters




### -param audioObjectType [out]

A value specifying the type of audio object that is represented 


## -returns



If the method succeeds, it returns S_OK.




## -remarks



Set the type of the audio object with the <i>type</i> parameter to the  <a href="https://msdn.microsoft.com/1B99E7FB-0796-4902-9B00-470FD08F8AFA">ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject</a> method.




## -see-also




<a href="https://msdn.microsoft.com/EE83AF5F-4342-4CF2-81A7-1123F8DAFA6F">ISpatialAudioObject</a>



<a href="https://msdn.microsoft.com/54721875-D93A-4C7E-A07E-C286E1A409D3">ISpatialAudioObjectBase</a>
 

 

