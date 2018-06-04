---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# SLPersistRTSPayloadOverride function


## -description


Associates information with the specified product for both online and phone activation.


## -parameters




### -param hSLC [in]

Type: <b>HSLC</b>

Handle retrieved by previous call to the <a href="https://msdn.microsoft.com/79a09cf3-cf6f-479a-89c7-27f5fcee3186">SLOpen</a> function.


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
 



