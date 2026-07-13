---
UID: NF:audioenginebaseapo.IApoAcousticEchoCancellation2.GetDesiredReferenceStreamProperties
tech.root: audio
title: IApoAcousticEchoCancellation2::GetDesiredReferenceStreamProperties
ms.date: 04/27/2023
targetos: Windows
description: Requests a set of properties for the loopback stream, if they are supported on the associated audio endpoint.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: audioenginebaseapo.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 26100
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - audioenginebaseapo.h
api_name:
 - IApoAcousticEchoCancellation2::GetDesiredReferenceStreamProperties
f1_keywords:
 - IApoAcousticEchoCancellation2::GetDesiredReferenceStreamProperties
 - audioenginebaseapo/IApoAcousticEchoCancellation2::GetDesiredReferenceStreamProperties
dev_langs:
 - c++
helpviewer_keywords:
 - GetDesiredReferenceStreamProperties
---

## -description

Callback function implemented by an APO that returns a set of requested loopback stream properties.

## -parameters

### -param pProperties [out]

A bitwise combination of flags from the [APO_REFERENCE_STREAM_PROPERTIES](ne-audioenginebaseapo-apo_reference_stream_properties.md) specifying the requested loopback stream properties.

## -returns

The **GetDesiredReferenceStreamProperties** method returns S_OK to indicate that it has completed successfully.

## -remarks

## -see-also

