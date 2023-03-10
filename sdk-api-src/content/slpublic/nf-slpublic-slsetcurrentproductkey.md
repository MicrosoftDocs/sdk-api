---
UID: NF:slpublic.SLSetCurrentProductKey
title: SLSetCurrentProductKey function (slpublic.h)
description: Sets the current product key to the previously installed product key.
helpviewer_keywords: ["SLSetCurrentProductKey","SLSetCurrentProductKey function [Security]","security.slsetcurrentproductkey","slpublic/SLSetCurrentProductKey"]
old-location: security\slsetcurrentproductkey.htm
tech.root: security
ms.assetid: a6490a89-9280-4b7d-8ea0-afa80c0a03f8
ms.date: 12/05/2018
ms.keywords: SLSetCurrentProductKey, SLSetCurrentProductKey function [Security], security.slsetcurrentproductkey, slpublic/SLSetCurrentProductKey
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
 - SLSetCurrentProductKey
 - slpublic/SLSetCurrentProductKey
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
 - SLSetCurrentProductKey
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

