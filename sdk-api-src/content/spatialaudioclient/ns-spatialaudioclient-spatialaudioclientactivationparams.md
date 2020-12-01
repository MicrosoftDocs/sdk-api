---
UID: NS:spatialaudioclient.SpatialAudioClientActivationParams
title: SpatialAudioClientActivationParams (spatialaudioclient.h)
description: Represents optional activation parameters for a spatial audio render stream. Pass this structure to ActivateAudioInterfaceAsync when activating an ISpatialAudioClient interface.
helpviewer_keywords: ["PSpatialAudioClientActivationParams","PSpatialAudioClientActivationParams structure pointer [Core Audio]","SpatialAudioClientActivationParams","SpatialAudioClientActivationParams structure [Core Audio]","coreaudio.spatialaudioclientactivationparams","spatialaudioclient/PSpatialAudioClientActivationParams","spatialaudioclient/SpatialAudioClientActivationParams"]
old-location: coreaudio\spatialaudioclientactivationparams.htm
tech.root: CoreAudio
ms.assetid: 6FEC7A70-D12E-4DB9-91DC-A54D5CCF8B57
ms.date: 12/05/2018
ms.keywords: PSpatialAudioClientActivationParams, PSpatialAudioClientActivationParams structure pointer [Core Audio], SpatialAudioClientActivationParams, SpatialAudioClientActivationParams structure [Core Audio], coreaudio.spatialaudioclientactivationparams, spatialaudioclient/PSpatialAudioClientActivationParams, spatialaudioclient/SpatialAudioClientActivationParams
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
req.typenames: SpatialAudioClientActivationParams
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SpatialAudioClientActivationParams
 - spatialaudioclient/SpatialAudioClientActivationParams
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - spatialaudioclient.h
api_name:
 - SpatialAudioClientActivationParams
---

# SpatialAudioClientActivationParams structure


## -description

Represents optional activation parameters for a spatial audio render stream. Pass this structure to <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync">ActivateAudioInterfaceAsync</a> when activating an <a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient">ISpatialAudioClient</a> interface.

## -struct-fields

### -field tracingContextId

An app-defined context identifier, used for event logging.

### -field appId

An identifier for the client app, used for event logging.



#### majorVersion

The major version number of the client app, used for event logging.



##### minorVersion1

The first minor version number of the client app, used for event logging.



###### minorVersion2

The second minor version number of the client app, used for event logging.



####### minorVersion3

The third minor version number of the client app, used for event logging.

### -field majorVersion

### -field minorVersion1

### -field minorVersion2

### -field minorVersion3

## -remarks

The following example code shows how to initialize this structure.


```cpp
PROPVARIANT var; 
PropVariantInit(&var);  
auto p = reinterpret_cast<SpatialAudioClientActivationParams *>(CoTaskMemAlloc(sizeof(SpatialAudioClientActivationParams)));  
if (nullptr == p) { ... } 
p->tracingContextId = /* context identifier */;  
p->appId = /* app identifier */;  
p->majorVersion = /* app version info */;  
p->majorVersionN = /* app version info */;
var.vt = VT_BLOB;
var.blob.cbSize = sizeof(*p);
var.blob.pBlobData = reinterpret_cast<BYTE *>(p); 
hr = ActivateAudioInterfaceAsync(device, __uuidof(ISpatialAudioClient), &var, ...);
// ...
ropVariantClear(&var);
```


To access the <b>ActivateAudioIntefaceAsync</b>, you will need to link to mmdevapi.lib.