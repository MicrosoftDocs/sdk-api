---
UID: NF:tdh.TdhEnumerateProvidersForDecodingSource
tech.root: ETW
title: TdhEnumerateProvidersForDecodingSource (tdh.h)
ms.date: 12/05/2022
ms.keywords: TdhEnumerateProvidersForDecodingSource
targetos: Windows
description: Retrieves a list of providers that have registered a MOF class or manifest file on the computer.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: tdh.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: OneCore.Lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11 [desktop apps only]
req.target-min-winversvr: Windows Server 2022 [desktop apps only]
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - api-ms-win-eventing-tdh-l1-1-2.dll
 - tdh.h
api_name:
 - TdhEnumerateProvidersForDecodingSource
f1_keywords:
 - TdhEnumerateProvidersForDecodingSource
 - tdh/TdhEnumerateProvidersForDecodingSource
dev_langs:
 - c++
helpviewer_keywords:
 - TdhEnumerateProvidersForDecodingSource
---

# TdhEnumerateProvidersForDecodingSource function (tdh.h)

## -description

Retrieves a list of providers that have registered a MOF class or manifest file on the computer.

## -parameters

### -param filter

One or more values from [DECODING_SOURCE enumeration](ne-tdh-decoding_source.md).

### -param buffer [out]

Array of providers that publicly define their events on the computer. For details, see the [PROVIDER_ENUMERATION_INFO structure](ns-tdh-provider_enumeration_info.md).

### -param bufferSize [in, out]

Size, in bytes, of the *pBuffer* buffer. If the function succeeds, this parameter receives the size of the buffer used. If the buffer is too small, the function returns ERROR_INSUFFICIENT_BUFFER and sets this parameter to the required buffer size. If the buffer size is zero on input, no data is returned in the buffer and this parameter receives the required buffer size.

### -param bufferRequired [out]

The buffer required.

## -returns

Returns ERROR_SUCCESS if successful. Otherwise, this function returns one of the following return codes in addition to others.

| Return code | Description |
| -- | -- |
| **ERROR_INSUFFICIENT_BUFFER**   | The size of the *pBuffer* buffer is too small. Use the required buffer size set in *pBufferSize* to allocate a new buffer.   |
| **ERROR_INVALID_PARAMETER** | One or more of the parameters is not valid. |

## -remarks

Use [TdhEnumerateProviders](nf-tdh-tdhenumerateproviders.md) to retrieve all providers that have registered on the computer.

## -see-also
