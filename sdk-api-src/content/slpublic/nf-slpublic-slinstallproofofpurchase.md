---
UID: NF:slpublic.SLInstallProofOfPurchase
title: SLInstallProofOfPurchase function (slpublic.h)
description: Registers the product key with SL.
helpviewer_keywords: ["SLInstallProofOfPurchase","SLInstallProofOfPurchase function [Security]","security.slinstallproofofpurchase","slpublic/SLInstallProofOfPurchase"]
old-location: security\slinstallproofofpurchase.htm
tech.root: security
ms.assetid: ea9efcf0-5146-4ede-8ec3-dc8617e34156
ms.date: 12/05/2018
ms.keywords: SLInstallProofOfPurchase, SLInstallProofOfPurchase function [Security], security.slinstallproofofpurchase, slpublic/SLInstallProofOfPurchase
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
 - SLInstallProofOfPurchase
 - slpublic/SLInstallProofOfPurchase
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
 - SLInstallProofOfPurchase
---

# SLInstallProofOfPurchase function


## -description

Registers the product key with SL.

## -parameters

### -param hSLC [in]

Type: <b>HSLC</b>

The handle to the current SLC context.

### -param pwszPKeyAlgorithm [in]

Type: <b>PCWSTR</b>

The product key algorithm.

### -param pwszPKeyString [in]

Type: <b>PCWSTR</b>

The product key string.

### -param cbPKeySpecificData [in]

Type: <b>UINT</b>

The size, in bytes, of product key specific data. If there is no PKey specific data, set <i>cbPKeySpecificData</i> to 0.

### -param pbPKeySpecificData [in, optional]

Type: <b>PBYTE</b>

A pointer to the product key specific data. If there is no PKey specific data, set <i>pbPKeySpecificData</i> to <b>NULL</b>.

### -param pPkeyId [out]

Type: <b>SLID*</b>

A pointer to an identifier of the registered product key. This <b>SLID</b> can be used to reference PKey information later.

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
</table>

