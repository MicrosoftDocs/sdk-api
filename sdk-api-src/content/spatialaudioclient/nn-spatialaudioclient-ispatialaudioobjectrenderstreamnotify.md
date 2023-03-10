---
UID: NN:spatialaudioclient.ISpatialAudioObjectRenderStreamNotify
title: ISpatialAudioObjectRenderStreamNotify (spatialaudioclient.h)
description: Provides notifications for spatial audio clients to respond to changes in the state of an ISpatialAudioObjectRenderStream.
helpviewer_keywords: ["ISpatialAudioObjectRenderStreamNotify","ISpatialAudioObjectRenderStreamNotify interface [Core Audio]","ISpatialAudioObjectRenderStreamNotify interface [Core Audio]","described","coreaudio.ispatialaudioobjectrenderstreamnotify","spatialaudioclient/ISpatialAudioObjectRenderStreamNotify"]
old-location: coreaudio\ispatialaudioobjectrenderstreamnotify.htm
tech.root: CoreAudio
ms.assetid: 3729D985-9040-43AD-A8B0-045509FE2F20
ms.date: 12/05/2018
ms.keywords: ISpatialAudioObjectRenderStreamNotify, ISpatialAudioObjectRenderStreamNotify interface [Core Audio], ISpatialAudioObjectRenderStreamNotify interface [Core Audio],described, coreaudio.ispatialaudioobjectrenderstreamnotify, spatialaudioclient/ISpatialAudioObjectRenderStreamNotify
req.header: spatialaudioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - ISpatialAudioObjectRenderStreamNotify
 - spatialaudioclient/ISpatialAudioObjectRenderStreamNotify
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
 - ISpatialAudioObjectRenderStreamNotify
---

# ISpatialAudioObjectRenderStreamNotify interface


## -description

Provides notifications for spatial audio clients to respond to changes in the state of an  <a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream">ISpatialAudioObjectRenderStream</a>. 

You register the object that implements this interface by assigning it to the <i>NotifyObject</i> parameter of the <a href="/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioclientactivationparams">SpatialAudioClientActivationParams</a> structure passed into the <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream">ISpatialAudioClient::ActivateSpatialAudioStream</a> method. After registering its <b>ISpatialAudioObjectRenderStreamNotify</b> interface, the client receives event notifications in the form of callbacks through the <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreamnotify-onavailabledynamicobjectcountchange">OnAvailableDynamicObjectCountChange</a> method in the interface.



This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.

## -inheritance

The <b>ISpatialAudioObjectRenderStreamNotify</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISpatialAudioObjectRenderStreamNotify</b> also has these types of members:

