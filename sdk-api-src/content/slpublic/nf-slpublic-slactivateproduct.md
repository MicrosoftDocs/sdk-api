---
UID: NF:slpublic.SLActivateProduct
title: SLActivateProduct function (slpublic.h)
description: Acquires a use license from the Software License Server (SLS).
helpviewer_keywords: ["SLActivateProduct","SLActivateProduct function [Security]","security.slactivateproduct","slpublic/SLActivateProduct"]
old-location: security\slactivateproduct.htm
tech.root: security
ms.assetid: 14a2e84f-f5f7-4f17-8c7c-2cf580e14a26
ms.date: 12/05/2018
ms.keywords: SLActivateProduct, SLActivateProduct function [Security], security.slactivateproduct, slpublic/SLActivateProduct
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
 - SLActivateProduct
 - slpublic/SLActivateProduct
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
 - SLActivateProduct
---

# SLActivateProduct function


## -description

Acquires a use license from the Software License Server (SLS).

## -parameters

### -param hSLC [in]

Type: <b>HSLC</b>

The handle to the current SLC context.

### -param pProductSkuId [in]

Type: <b>const SLID*</b>

 A pointer to the product ID.

### -param cbAppSpecificData [in, optional]

Type: <b>UINT</b>

The size of application specific data.

### -param pvAppSpecificData [in, optional]

Type: <b>const PVOID</b>

A pointer to application specific data. The license server can use this     
		information to embed application specific run-time information.

### -param pActivationInfo [in, optional]

Type: <b>const <a href="/windows/desktop/api/slpublic/ns-slpublic-sl_activation_info_header">SL_ACTIVATION_INFO_HEADER</a>*</b>

A pointer to additional product activation information.

### -param pwszProxyServer [in, optional]

Type: <b>PCWSTR</b>

The proxy server name. Set this to <b>NULL</b> to use automatic proxy discovery.

### -param wProxyPort [in, optional]

Type: <b>WORD</b>

The proxy server port. To use the default port, set <i>wProxyPort</i> to 0.

## -returns

Type: <b>HRESULT WINAPI</b>

If this function succeeds, it return <b>S_OK</b>.  Otherwise,  it returns an <b>HRESULT</b> error code.

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
<dt><b>SL_E_PUBLISHING_LICENSE_NOT_INSTALLED</b></dt>
<dt>0xC004F017</dt>
</dl>
</td>
<td width="60%">
The license is not installed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_PKEY_NOT_INSTALLED</b></dt>
<dt>0xC004F014
</dt>
</dl>
</td>
<td width="60%">
The product key is not available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_PRODUCT_SKU_NOT_INSTALLED</b></dt>
<dt>0xc004f015</dt>
</dl>
</td>
<td width="60%">
The license is not installed.

</td>
</tr>
</table>