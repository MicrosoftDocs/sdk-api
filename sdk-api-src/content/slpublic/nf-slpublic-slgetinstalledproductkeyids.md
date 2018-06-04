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

# SLGetInstalledProductKeyIds function


## -description


This function returns a list of product key IDs associated     
	with the specified Product SKU ID.


## -parameters




### -param hSLC [in]

Type: <b>HSLC</b>

The handle to the current SLC session.


### -param pProductSkuId [in]

Type: <b>const SLID*</b>

A pointer to the product SKU ID.


### -param pnProductKeyIds [out]

Type: <b>UINT*</b>

A pointer to the number of product Key IDs returned.


### -param ppProductKeyIds [out]

Type: <b>SLID**</b>

A pointer to an array of the product Key IDs.


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
<dt><b>SL_E_VALUE_NOT_FOUND</b></dt>
<dt>0xC004F012</dt>
</dl>
</td>
<td width="60%">
The value for the input key was not found.

</td>
</tr>
</table>
 



