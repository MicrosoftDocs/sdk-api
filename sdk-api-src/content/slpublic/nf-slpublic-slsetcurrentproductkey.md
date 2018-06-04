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

# SLSetCurrentProductKey function


## -description


Sets the current      
	product key to the previously installed product key.


## -parameters




### -param hSLC [in]

Type: <b>HSLC</b>

The handle to the current SLC context.


### -param pProductSkuId [in]

Type: <b>const SLID*</b>

A pointer to the product SKU ID.


### -param pProductKeyId [in]

Type: <b>const SLID*</b>

A pointer to the product key ID.


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
<dt><b>SL_E_MISMATCHED_PRODUCT_SKU</b></dt>
<dt>0xC004F069</dt>
</dl>
</td>
<td width="60%">
The product SKU is not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_PKEY_NOT_INSTALLED</b></dt>
<dt>0xC004F014</dt>
</dl>
</td>
<td width="60%">
The product key is not available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_OPERATION_NOT_ALLOWED</b></dt>
<dt>0xC004F06A</dt>
</dl>
</td>
<td width="60%">
The requested operation is not allowed.

</td>
</tr>
</table>
 



