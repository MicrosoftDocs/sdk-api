---
UID: NF:slpublic.SLPersistRTSPayloadOverride
title: SLPersistRTSPayloadOverride function (slpublic.h)
description: Associates information with the specified product for both online and phone activation.
helpviewer_keywords: ["SLPersistRTSPayloadOverride","SLPersistRTSPayloadOverride function [Security]","security.slpersistrtspayloadoverride","slpublic/SLPersistRTSPayloadOverride"]
old-location: security\slpersistrtspayloadoverride.htm
tech.root: security
ms.assetid: d053c9dc-c719-4e0c-b1e9-58303b51cb26
ms.date: 12/05/2018
ms.keywords: SLPersistRTSPayloadOverride, SLPersistRTSPayloadOverride function [Security], security.slpersistrtspayloadoverride, slpublic/SLPersistRTSPayloadOverride
req.header: slpublic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Slc.lib
req.dll: Slc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SLPersistRTSPayloadOverride
 - slpublic/SLPersistRTSPayloadOverride
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Slc.dll
api_name:
 - SLPersistRTSPayloadOverride
---

# SLPersistRTSPayloadOverride function


## -description

Associates information with the specified product for both online and phone activation.

## -parameters

### -param hSLC [in]

Type: <b>HSLC</b>

Handle retrieved by previous call to the <a href="/windows/desktop/api/slpublic/nf-slpublic-slopen">SLOpen</a> function.

### -param pApplicationId [in]

Type: <b>const SLID*</b>

A pointer to the identifier of the application ID to be used for the fast policy queries.

### -param pProductSkuId [in, optional]

Type: <b>const SLID*</b>

A pointer to the identifier of the ACID to be used for the fast policy queries.

### -param pbData [in]

Type: <b>BYTE*</b>

A pointer to the byte data that will be sent during activation.

This function assumes the data is composed of a 20-bit value stored in the first three bytes:      
		Byte[0] is the LSB of the HIWORD, Byte[1] is the HSB of the LOWORD, and Byte[2] is the LSB of the LOWORD.   
		Any value composed of these three bytes that exceeds 20 bits will be rejected with <b>E_INVALIDARG</b>.

### -param cbData [in]

Type: <b>DWORD</b>

The number of bytes that will be stored.  This must be set to 3.

## -returns

Type: <b>HRESULT WINAPI</b>

If this function succeeds, it return <b>S_OK</b>.  Otherwise, it returns an <b>HRESULT</b> error code.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
<dt>0x80070057</dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

</td>
</tr>
</table>