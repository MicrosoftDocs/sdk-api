---
UID: NN:audioenginebaseapo.IApoAcousticEchoCancellation
tech.root: audio
title: IApoAcousticEchoCancellation
ms.date: 02/17/2021
ms.topic: language-reference
targetos: Windows
description: This interface is implemented by APOs to enable acoustic echo cancellation (AEC) scenarios. 
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: audioenginebaseapo.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: 
req.target-type: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - audioenginebaseapo.h
api_name:
 - IApoAcousticEchoCancellation
f1_keywords:
 - IApoAcousticEchoCancellation
 - audioenginebaseapo/IApoAcousticEchoCancellation
helpviewer_keywords:
 - IApoAcousticEchoCancellation
 - audioenginebaseapo/IApoAcousticEchoCancellation
dev_langs:
 - c++
---

## -description

This interface is implemented by APOs to enable acoustic echo cancellation (AEC) scenarios. 

## -remarks

This interface may only be implemented by mode effects (MFX) on capture endpoints. Implementing this interface on any other APO will lead to a failure in loading that APO. If the mode effect on a capture endpoint is implemented as a series of chained APOs, only the APO closest to the device may implement this interface.

The **IApoAcousticEchoCancellation** interface has no explicit methods on it. Its purpose is to identify an AEC APO to the audio engine. APOs that implement this interface will be passed an [APO_CONNECTION_PROPERTY_V2](/windows/win32/api/audioapotypes/ns-audioapotypes-apo_connection_property_v2) structure in its call to [IAudioProcessingObjectRT::APOProcess](nf-audioenginebaseapo-iaudioprocessingobjectrt-apoprocess.md). **APO_CONNECTION_PROPERTY_V2** provides a timestamp to allow the APO to synchronize buffers from the primary and auxiliary streams. If the **u32Signature** field of the [APO_CONNECTION_PROPERTY](/windows/win32/api/audioapotypes/ns-audioapotypes-apo_connection_property) structure passed into **IAudioProcessingObjectRT::APOProcess** is equal to **APO_CONNECTION_PROPERTY_V2_SIGNATURE**, the structure can be safely typecast to a **APO_CONNECTION_PROPERTY_V2**.

Because AEC algorithms typically require specific sampling rates and channel counts, the audio engine provides resampling support to APOs that implement the **IApoAcousticEchoCancellation** interface. The [IApoAuxiliaryInputConfiguration::IsInputFormatSupported](nf-audioenginebaseapo-iapoauxiliaryinputconfiguration-isinputformatsupported.md) method provides a mechanism for informing the system of the APO's preferred input format by returning the HRESULT APOERR_FORMAT_NOT_SUPPORTED. and returning the requested format in the method's *ppSupportedInputFormat* parameter. The audio engine will then resample input audio to the suggested format prior to sending it to the AEC APO. This eliminates the need for the AEC APO to implement sampling rate and channel count conversion.


## -see-also
[APO_CONNECTION_PROPERTY_V2](/windows/win32/api/audioapotypes/ns-audioapotypes-apo_connection_property_v2)
[IAudioProcessingObjectRT::APOProcess](nf-audioenginebaseapo-iaudioprocessingobjectrt-apoprocess.md)
[IAudioProcessingObject::IsInputFormatSupported](nf-audioenginebaseapo-iapoauxiliaryinputconfiguration-isinputformatsupported.md)

