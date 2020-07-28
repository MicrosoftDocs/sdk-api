---
UID: NF:spatialaudioclient.ISpatialAudioClient.GetMaxDynamicObjectCount
title: ISpatialAudioClient::GetMaxDynamicObjectCount (spatialaudioclient.h)
description: Gets the maximum number of dynamic audio objects for the spatial audio client.
helpviewer_keywords: ["GetMaxDynamicObjectCount","GetMaxDynamicObjectCount method [Core Audio]","GetMaxDynamicObjectCount method [Core Audio]","ISpatialAudioClient interface","ISpatialAudioClient interface [Core Audio]","GetMaxDynamicObjectCount method","ISpatialAudioClient.GetMaxDynamicObjectCount","ISpatialAudioClient::GetMaxDynamicObjectCount","coreaudio.ispatialaudioclient_getmaxdynamicobjectcount","spatialaudioclient/ISpatialAudioClient::GetMaxDynamicObjectCount"]
old-location: coreaudio\ispatialaudioclient_getmaxdynamicobjectcount.htm
tech.root: CoreAudio
ms.assetid: 0185D09E-0009-41BF-A0BB-3C3CE0A69BA8
ms.date: 12/05/2018
ms.keywords: GetMaxDynamicObjectCount, GetMaxDynamicObjectCount method [Core Audio], GetMaxDynamicObjectCount method [Core Audio],ISpatialAudioClient interface, ISpatialAudioClient interface [Core Audio],GetMaxDynamicObjectCount method, ISpatialAudioClient.GetMaxDynamicObjectCount, ISpatialAudioClient::GetMaxDynamicObjectCount, coreaudio.ispatialaudioclient_getmaxdynamicobjectcount, spatialaudioclient/ISpatialAudioClient::GetMaxDynamicObjectCount
f1_keywords:
- spatialaudioclient/ISpatialAudioClient.GetMaxDynamicObjectCount
dev_langs:
- c++
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
- ISpatialAudioClient.GetMaxDynamicObjectCount
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISpatialAudioClient::GetMaxDynamicObjectCount


## -description


Gets the maximum number of dynamic audio objects for the spatial audio client.


## -parameters




### -param value [out]

Gets the maximum dynamic object count for this client.


## -returns



If the method succeeds, it returns S_OK.




## -remarks



A dynamic <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject">ISpatialAudioObject</a> is one that was activated by setting the <i>type</i> parameter to the  <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject">ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject</a> method to <b>AudioObjectType_Dynamic</b>. The client has a limit of the maximum number of dynamic spatial audio objects that can be activated at one time. When the capacity of the audio rendering pipeline changes, the system will dynamically adjust the maximum number of concurrent dynamic spatial audio objects. Before doing so, the system will call <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreamnotify-onavailabledynamicobjectcountchange">OnAvailableDynamicObjectCountChange</a> to notify clients of the resource limit change. 

Call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on an <b>ISpatialAudioObject</b> when it is no longer being used to free up the resource to create new dynamic spatial audio objects.

When Windows Sonic is not available (for instance, when playing to embedded laptop stereo speakers, or if the user has not explicitly enabled Windows Sonic on the device), the number of available dynamic objects returned by <b>GetMaxDynamicObjectCount</b> to an application will be 0.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient">ISpatialAudioClient</a>
 

 

