---
UID: NF:slpublic.SLGetPKeyInformation
title: SLGetPKeyInformation function (slpublic.h)
description: Gets the information of the specified product key.
helpviewer_keywords: ["SLGetPKeyInformation","SLGetPKeyInformation function [Security]","SL_DATA_BINARY","SL_DATA_DWORD","SL_DATA_SZ","SL_INFO_KEY_CHANNEL","SL_INFO_KEY_DIGITAL_PID","SL_INFO_KEY_DIGITAL_PID2","SL_INFO_KEY_PARTIAL_PRODUCT_KEY","SL_INFO_KEY_PRODUCT_SKU_ID","security.slgetpkeyinformation","slpublic/SLGetPKeyInformation"]
old-location: security\slgetpkeyinformation.htm
tech.root: security
ms.assetid: b7728d20-da39-4443-aaca-a6461880bb53
ms.date: 12/05/2018
ms.keywords: SLGetPKeyInformation, SLGetPKeyInformation function [Security], SL_DATA_BINARY, SL_DATA_DWORD, SL_DATA_SZ, SL_INFO_KEY_CHANNEL, SL_INFO_KEY_DIGITAL_PID, SL_INFO_KEY_DIGITAL_PID2, SL_INFO_KEY_PARTIAL_PRODUCT_KEY, SL_INFO_KEY_PRODUCT_SKU_ID, security.slgetpkeyinformation, slpublic/SLGetPKeyInformation
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
 - SLGetPKeyInformation
 - slpublic/SLGetPKeyInformation
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
 - SLGetPKeyInformation
---

# SLGetPKeyInformation function


## -description

Gets the information of the specified product key.

## -parameters

### -param hSLC [in]

Type: <b>HSLC</b>

The handle to the current SLC context.

### -param pPKeyId [in]

Type: <b>const SLID*</b>

A pointer to the PKey ID.

### -param pwszValueName [in]

Type: <b>PCWSTR</b>

The name associated with the value to retrieve.  The following names are valid.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SL_INFO_KEY_DIGITAL_PID"></a><a id="sl_info_key_digital_pid"></a><dl>
<dt><b>SL_INFO_KEY_DIGITAL_PID</b></dt>
<dt>L"DigitalPID" </dt>
</dl>
</td>
<td width="60%">
Formatted PID structure for a PID4

</td>
</tr>
<tr>
<td width="40%"><a id="SL_INFO_KEY_DIGITAL_PID2"></a><a id="sl_info_key_digital_pid2"></a><dl>
<dt><b>SL_INFO_KEY_DIGITAL_PID2</b></dt>
<dt>L"DigitalPID2"</dt>
</dl>
</td>
<td width="60%">
Formatted PID structure for a PID2

</td>
</tr>
<tr>
<td width="40%"><a id="SL_INFO_KEY_PARTIAL_PRODUCT_KEY"></a><a id="sl_info_key_partial_product_key"></a><dl>
<dt><b>SL_INFO_KEY_PARTIAL_PRODUCT_KEY</b></dt>
<dt>L"PartialProductKey"</dt>
</dl>
</td>
<td width="60%">
First 5 characters of product key

</td>
</tr>
<tr>
<td width="40%"><a id="SL_INFO_KEY_PRODUCT_SKU_ID"></a><a id="sl_info_key_product_sku_id"></a><dl>
<dt><b>SL_INFO_KEY_PRODUCT_SKU_ID</b></dt>
<dt>L"ProductSkuId"</dt>
</dl>
</td>
<td width="60%">
SKU SLID

</td>
</tr>
<tr>
<td width="40%"><a id="SL_INFO_KEY_CHANNEL"></a><a id="sl_info_key_channel"></a><dl>
<dt><b>SL_INFO_KEY_CHANNEL</b></dt>
<dt>L"Channel" </dt>
</dl>
</td>
<td width="60%">
Channel ID

</td>
</tr>
</table>

### -param peDataType [out, optional]

Type: <b><a href="/windows/desktop/api/slpublic/ne-slpublic-sldatatype">SLDATATYPE</a>*</b>

The data type.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SL_DATA_SZ"></a><a id="sl_data_sz"></a><dl>
<dt><b>SL_DATA_SZ</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
UNICODE string

</td>
</tr>
<tr>
<td width="40%"><a id="SL_DATA_DWORD"></a><a id="sl_data_dword"></a><dl>
<dt><b>SL_DATA_DWORD</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
DWORD

</td>
</tr>
<tr>
<td width="40%"><a id="SL_DATA_BINARY"></a><a id="sl_data_binary"></a><dl>
<dt><b>SL_DATA_BINARY</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Binary BLOB

</td>
</tr>
</table>

### -param pcbValue [out]

Type: <b>UINT*</b>

A pointer to the size, in bytes, of the <i>ppbValue</i> buffer.

### -param ppbValue [out]

Type: <b>PBYTE*</b>

A pointer to the data returned by SLC.          
		When finished using the memory, free it by calling the <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function.

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
<dt><b>SL_E_NOT_SUPPORTED</b></dt>
<dt>0xC004F016</dt>
</dl>
</td>
<td width="60%">
The request is not supported.

</td>
</tr>
</table>