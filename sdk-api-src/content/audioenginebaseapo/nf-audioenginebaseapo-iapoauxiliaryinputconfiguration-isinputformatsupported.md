---
UID: NF:audioenginebaseapo.IApoAuxiliaryInputConfiguration.IsInputFormatSupported
tech.root: audio
title: IApoAuxiliaryInputConfiguration::IsInputFormatSupported
ms.date: 02/17/2021
ms.topic: language-reference
targetos: Windows
description: Verifies that a specific auxiliary input format is supported by the APO.
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
req.target-min-winverclnt: Windows 10 Build 20348
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
 - IApoAuxiliaryInputConfiguration::IsInputFormatSupported
f1_keywords:
 - IApoAuxiliaryInputConfiguration::IsInputFormatSupported
 - audioenginebaseapo/IApoAuxiliaryInputConfiguration::IsInputFormatSupported
helpviewer_keywords:
 - IApoAuxiliaryInputConfiguration::IsInputFormatSupported
 - audioenginebaseapo/IApoAuxiliaryInputConfiguration::IsInputFormatSupported
dev_langs:
 - c++
---

## -description

Verifies that a specific auxiliary input format is supported by the APO.

## -parameters

### -param pRequestedInputFormat

The input format that is to be verified.

### -param ppSupportedInputFormat

The APO populates this parameter with the supported input format closest to the format passed in to the method.

## -returns

HRESULT 

| HRESULT | Description | 
|---------------|--------------|
| S_OK | Successful completion. The APO should add a reference to *pRequestedInputFormat* and return it in *ppSupportedInputFormat* |
| S_FALSE | Format is not supported. The APO should return a suggested supported format in *ppSupportedInputFormat* |
| APOERR_FORMAT_NOT_SUPPORTED | Format is not supported. The APO should not modify *ppSupportedInputFormat*|
| E_POINTER | Invalid pointer passed to this function. |
| Other values | Another component is causing a failure. These failures are tracked by the system. |



## -remarks

If the APO can accept the requested format, it should add a reference to the requested format, return this as the supported output format, and return S_OK.

If the APO cannot accept the requested format it may suggest an alternate requested format.  In this case it should create and return the suggested format, and return S_FALSE.

The returned supported format should be 'closest' to the requested format, meaning that the format should have the same values for the following properties, specified in priority order.

- sample format
- bit depth
- number of channels
- sample rate 

The suggested format may only be different from the requested format if S_FALSE is returned. When returning any failure, the suggested format should be left untouched.

This API may be called at any time. The returned results will depend on the internal state of the APO which may
be manipulated by external user-interfaces.  Once the APO is locked for processing, however, this format cannot and will not changed.

This method may not be called from a real-time processing thread.


## -see-also

