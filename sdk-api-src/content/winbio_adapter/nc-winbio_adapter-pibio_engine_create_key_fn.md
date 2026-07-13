---
UID: NC:winbio_adapter.PIBIO_ENGINE_CREATE_KEY_FN
title: PIBIO_ENGINE_CREATE_KEY_FN (winbio_adapter.h)
description: Called by the Windows Biometric Framework to push an HMAC key to the sensor. The returned key identifier will be passed back to the biometric unit when the framework calls EngineAdapterIdentifyFeatureSetSecure.
helpviewer_keywords: ["EngineAdapterCreateKey","EngineAdapterCreateKey callback function [Windows Biometric Framework API]","PIBIO_ENGINE_CREATE_KEY_FN","PIBIO_ENGINE_CREATE_KEY_FN callback","secbiomet.engineadaptercreatekey","winbio_adapter/EngineAdapterCreateKey"]
old-location: secbiomet\engineadaptercreatekey.htm
tech.root: SecBioMet
ms.assetid: 3EB42081-6949-46F8-B235-377234A90C39
ms.date: 12/05/2018
ms.keywords: EngineAdapterCreateKey, EngineAdapterCreateKey callback function [Windows Biometric Framework API], PIBIO_ENGINE_CREATE_KEY_FN, PIBIO_ENGINE_CREATE_KEY_FN callback, secbiomet.engineadaptercreatekey, winbio_adapter/EngineAdapterCreateKey
req.header: winbio_adapter.h
req.include-header: Winbio_adapter.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
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
 - PIBIO_ENGINE_CREATE_KEY_FN
 - winbio_adapter/PIBIO_ENGINE_CREATE_KEY_FN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winbio_adapter.h
api_name:
 - EngineAdapterCreateKey
---

# PIBIO_ENGINE_CREATE_KEY_FN callback function


## -description



Called by the Windows Biometric Framework to push an HMAC key to the sensor. The returned key identifier will be passed back to the biometric unit when the framework calls <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_secure_fn">EngineAdapterIdentifyFeatureSetSecure</a>.

## -parameters

### -param Pipeline

Pointer to a <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

### -param Key

Pointer to a buffer that contains the HMAC key.

### -param KeySize

Size, in bytes, of the buffer specified by the <b>Key</b>  parameter.

### -param KeyIdentifier

Pointer to a buffer that receives a key identifier. The format of the buffer is vendor-defined.

### -param KeyIdentifierSize

Size, in bytes, of the buffer specified by the <b>KeyIdentifier</b>  parameter.

### -param ResultSize

Pointer to a variable that receives the size, in bytes, of the data written to the buffer specified by the <b>KeyIdentifier</b>  parameter.

## -returns

If the <b>KeyIdentifier</b> buffer is too small, <b>WINBIO_E_KEY_IDENTIFIER_BUFFER_TOO_SMALL</b> must be returned, and the required size must be written to <i>ResultSize</i>. The framework will call the API again with a larger buffer.
If the sensor cannot create the key, <b>WINBIO_E_KEY_CREATION_FAILED</b> must be returned.

## -remarks

Only a single key will be in use at any time. If <b>EngineAdapterCreateKey</b> is called when the engine has knowledge of a preexisting key, the preexisting key must be overwritten with the new one.
