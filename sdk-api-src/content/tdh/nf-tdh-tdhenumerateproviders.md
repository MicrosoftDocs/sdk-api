---
UID: NF:tdh.TdhEnumerateProviders
title: TdhEnumerateProviders function (tdh.h)
description: Retrieves a list of providers that have registered a MOF class or manifest file on the computer.
helpviewer_keywords: ["TdhEnumerateProviders","TdhEnumerateProviders function [ETW]","etw.tdhenumerateproviders_func","tdh.tdhenumerateproviders_func","tdh/TdhEnumerateProviders"]
old-location: etw\tdhenumerateproviders_func.htm
tech.root: ETW
ms.assetid: ef326ef8-227d-46b5-88b9-b519748fb778
ms.date: 12/05/2018
ms.keywords: TdhEnumerateProviders, TdhEnumerateProviders function [ETW], etw.tdhenumerateproviders_func, tdh.tdhenumerateproviders_func, tdh/TdhEnumerateProviders
req.header: tdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Tdh.lib
req.dll: Tdh.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TdhEnumerateProviders
 - tdh/TdhEnumerateProviders
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-eventing-tdh-l1-1-2.dll
 - api-ms-win-eventing-tdh-l1-1-1.dll
 - Tdh.dll
 - API-MS-Win-Eventing-Tdh-L1-1-0.dll
 - MinTdh.dll
api_name:
 - TdhEnumerateProviders
---

# TdhEnumerateProviders function

## -description

Retrieves a list of all providers that have registered on the computer.

## -parameters

### -param pBuffer [out]

Array of providers that publicly define  their events on the computer. For details, see the <a href="/windows/desktop/api/tdh/ns-tdh-provider_enumeration_info">PROVIDER_ENUMERATION_INFO</a> structure.

### -param pBufferSize [in, out]

Size, in bytes, of the *pBuffer* buffer. If the function succeeds, this parameter receives the size of the buffer used. If the buffer is too small, the function returns ERROR_INSUFFICIENT_BUFFER and sets this parameter to the required buffer size. If the buffer size is zero on input, no data is returned in the buffer and this parameter receives the required buffer size.

## -returns

Returns ERROR_SUCCESS if successful. Otherwise, this function returns one of the following return codes in addition to others.

| Return code | Description |
| -- | -- |
| **ERROR_INSUFFICIENT_BUFFER**   | The size of the *pBuffer* buffer is too small. Use the required buffer size set in *pBufferSize* to allocate a new buffer.   |
| **ERROR_INVALID_PARAMETER** | One or more of the parameters is not valid. |

## -remarks

Call [TdhEnumerateProvidersForDecodingSource function](nf-tdh-tdhenumerateprovidersfordecodingsource.md) to retrieve a list of providers that have registered a MOF class or manifest file on the computer.

Because the number of registered event providers may fluctuate between calls to  this function, you should place this function in a loop that loops until the returned value is no longer ERROR_INSUFFICIENT_BUFFER.

### Examples

For an example that shows how to enumerate providers, see <a href="/windows/desktop/ETW/enumerating-providers">Enumerating Providers</a>.

## -see-also
<a href="/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfieldinformation">TdhEnumerateProviderFieldInformation</a>