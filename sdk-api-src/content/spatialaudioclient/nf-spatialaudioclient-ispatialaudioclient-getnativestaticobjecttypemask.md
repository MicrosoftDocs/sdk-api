---
UID: NF:spatialaudioclient.ISpatialAudioClient.GetNativeStaticObjectTypeMask
title: ISpatialAudioClient::GetNativeStaticObjectTypeMask (spatialaudioclient.h)
description: Gets a channel mask which represents the subset of static speaker bed channels native to current rendering engine.
helpviewer_keywords: ["GetNativeStaticObjectTypeMask","GetNativeStaticObjectTypeMask method [Core Audio]","GetNativeStaticObjectTypeMask method [Core Audio]","ISpatialAudioClient interface","ISpatialAudioClient interface [Core Audio]","GetNativeStaticObjectTypeMask method","ISpatialAudioClient.GetNativeStaticObjectTypeMask","ISpatialAudioClient::GetNativeStaticObjectTypeMask","coreaudio.ispatialaudioclient_getnativestaticobjecttypemask","spatialaudioclient/ISpatialAudioClient::GetNativeStaticObjectTypeMask"]
old-location: coreaudio\ispatialaudioclient_getnativestaticobjecttypemask.htm
tech.root: CoreAudio
ms.assetid: 29963682-AD45-4CEC-81A0-4B834505F9D5
ms.date: 12/05/2018
ms.keywords: GetNativeStaticObjectTypeMask, GetNativeStaticObjectTypeMask method [Core Audio], GetNativeStaticObjectTypeMask method [Core Audio],ISpatialAudioClient interface, ISpatialAudioClient interface [Core Audio],GetNativeStaticObjectTypeMask method, ISpatialAudioClient.GetNativeStaticObjectTypeMask, ISpatialAudioClient::GetNativeStaticObjectTypeMask, coreaudio.ispatialaudioclient_getnativestaticobjecttypemask, spatialaudioclient/ISpatialAudioClient::GetNativeStaticObjectTypeMask
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
 - ISpatialAudioClient::GetNativeStaticObjectTypeMask
 - spatialaudioclient/ISpatialAudioClient::GetNativeStaticObjectTypeMask
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
 - ISpatialAudioClient.GetNativeStaticObjectTypeMask
---

# ISpatialAudioClient::GetNativeStaticObjectTypeMask


## -description

Gets a  channel mask which represents the subset of static speaker bed channels native to current rendering engine.

## -parameters

### -param mask [out]

A bitwise combination of values from the <a href="/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype">AudioObjectType</a> enumeration indicating a subset of static speaker channels. The values returned will only include the static channel values and will not include <b>AudioObjectType_Dynamic</b>.

## -returns

If the method succeeds, it returns S_OK.

## -see-also

<a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient">ISpatialAudioClient</a>