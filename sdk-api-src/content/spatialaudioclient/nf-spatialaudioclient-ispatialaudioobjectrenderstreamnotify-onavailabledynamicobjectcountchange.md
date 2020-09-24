---
UID: NF:spatialaudioclient.ISpatialAudioObjectRenderStreamNotify.OnAvailableDynamicObjectCountChange
title: ISpatialAudioObjectRenderStreamNotify::OnAvailableDynamicObjectCountChange (spatialaudioclient.h)
description: Notifies the spatial audio client when the rendering capacity for an ISpatialAudioObjectRenderStream is about to change, specifies the time after which the change will occur, and specifies the number of dynamic audio objects that will be available after the change.
helpviewer_keywords: ["ISpatialAudioObjectRenderStreamNotify interface [Core Audio]","OnAvailableDynamicObjectCountChange method","ISpatialAudioObjectRenderStreamNotify.OnAvailableDynamicObjectCountChange","ISpatialAudioObjectRenderStreamNotify::OnAvailableDynamicObjectCountChange","OnAvailableDynamicObjectCountChange","OnAvailableDynamicObjectCountChange method [Core Audio]","OnAvailableDynamicObjectCountChange method [Core Audio]","ISpatialAudioObjectRenderStreamNotify interface","coreaudio.ispatialaudioobjectrenderstreamnotify_onavailabledynamicobjectcountchange","spatialaudioclient/ISpatialAudioObjectRenderStreamNotify::OnAvailableDynamicObjectCountChange"]
old-location: coreaudio\ispatialaudioobjectrenderstreamnotify_onavailabledynamicobjectcountchange.htm
tech.root: CoreAudio
ms.assetid: BC3F1171-26BC-46D0-8AE2-6BCD2393D617
ms.date: 12/05/2018
ms.keywords: ISpatialAudioObjectRenderStreamNotify interface [Core Audio],OnAvailableDynamicObjectCountChange method, ISpatialAudioObjectRenderStreamNotify.OnAvailableDynamicObjectCountChange, ISpatialAudioObjectRenderStreamNotify::OnAvailableDynamicObjectCountChange, OnAvailableDynamicObjectCountChange, OnAvailableDynamicObjectCountChange method [Core Audio], OnAvailableDynamicObjectCountChange method [Core Audio],ISpatialAudioObjectRenderStreamNotify interface, coreaudio.ispatialaudioobjectrenderstreamnotify_onavailabledynamicobjectcountchange, spatialaudioclient/ISpatialAudioObjectRenderStreamNotify::OnAvailableDynamicObjectCountChange
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISpatialAudioObjectRenderStreamNotify::OnAvailableDynamicObjectCountChange
 - spatialaudioclient/ISpatialAudioObjectRenderStreamNotify::OnAvailableDynamicObjectCountChange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - spatialaudioclient.h
api_name:
 - ISpatialAudioObjectRenderStreamNotify.OnAvailableDynamicObjectCountChange
---

# ISpatialAudioObjectRenderStreamNotify::OnAvailableDynamicObjectCountChange


## -description

Notifies the spatial audio client when the rendering capacity for an <a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream">ISpatialAudioObjectRenderStream</a> is about to change, specifies the time after which the change will occur, and specifies the number of dynamic audio objects that will be available after the change.

## -parameters

### -param sender [in]

The spatial audio render stream for which the available dynamic object count is changing.

### -param hnsComplianceDeadlineTime [in]

The time after which the spatial resource limit will change, in 100-nanosecond units. A value of  0 means that the change will occur immediately.

### -param availableDynamicObjectCountChange [in]

The number of dynamic spatial audio objects that will be available to the stream after <i>hnsComplianceDeadlineTime</i>.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

A dynamic <a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject">ISpatialAudioObject</a> is one that was activated by setting the <i>type</i> parameter to the  <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject">ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject</a> method to <b>AudioObjectType_Dynamic</b>. The client has a limit of the maximum number of dynamic spatial audio objects that can be activated at one time. When the capacity of the audio rendering pipeline changes, the system will dynamically adjust the maximum number of concurrent dynamic spatial audio objects. Before doing so, the system will call <b>OnAvailableDynamicObjectCountChange</b> to notify clients of the resource limit change. 

Call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on an <b>ISpatialAudioObject</b> when it is no longer being used to free up the resource to create new dynamic spatial audio objects.

## -see-also

<a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstreamnotify">ISpatialAudioObjectRenderStreamNotify</a>