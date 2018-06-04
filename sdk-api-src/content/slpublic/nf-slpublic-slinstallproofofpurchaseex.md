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

# SLInstallProofOfPurchaseEx function


## -description


Register the product key with SL.


## -parameters




### -param hSLC [in]

Type: <b>HSLC</b>

The handle to the current SLC context.


### -param pApplicationId [in]

Type: <b>const SLID*</b>

A pointer to the application ID.


### -param pProductSkuId [in, optional]

Type: <b>const SLID*</b>

A pointer to the product SKU ID.


### -param pwszPKeyAlgorithm [in]

Type: <b>PCWSTR</b>

The product key algorithm.


### -param pwszPKeyString [in]

Type: <b>PCWSTR</b>

The product key string.


### -param cbPKeySpecificData [in]

Type: <b>UINT</b>

The size, in bytes, of the product key specific data. If no PKey specific data exists, set <i>cbPKeySpecificData</i> to 0.


### -param pbPKeySpecificData [in, optional]

Type: <b>PBYTE</b>

A pointer to product key specific data. If no PKey specific data exists, set <i>pbPKeySpecificData</i> to <b>NULL</b>.


### -param pPkeyId

TBD




#### - pPKeyId [out]

Type: <b>SLID*</b>

A pointer to the  identifier of the registered product key. Used to reference PKey information.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
<dt>0x80070005</dt>
</dl>
</td>
<td width="60%">
Access denied (API requires admin privileges).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_LUA_ACCESSDENIED</b></dt>
<dt>0xC004F025</dt>
</dl>
</td>
<td width="60%">
The action requires administrator privilege.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_INVALID_PKEY</b></dt>
<dt>0xC004F010</dt>
</dl>
</td>
<td width="60%">
The product key is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_PRODUCT_SKU_NOT_INSTALLED</b></dt>
<dt>0xC004F015</dt>
</dl>
</td>
<td width="60%">
The license is not installed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_PKEY_INVALID_UPGRADE</b></dt>
<dt>0xC004F061</dt>
</dl>
</td>
<td width="60%">
This specified product key can only be used for upgrading, not for clean installations.

</td>
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
</table>
 



