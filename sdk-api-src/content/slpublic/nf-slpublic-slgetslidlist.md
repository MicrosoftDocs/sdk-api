---
UID: NF:slpublic.SLGetSLIDList
title: SLGetSLIDList function (slpublic.h)
description: Gets a list of SLIDs according to the input query ID type and the ID value.
helpviewer_keywords: ["SLGetSLIDList","SLGetSLIDList function [Security]","security.slgetslidlist","slpublic/SLGetSLIDList"]
old-location: security\slgetslidlist.htm
tech.root: security
ms.assetid: e2733f2e-e78b-4a77-a81d-d5913baa4bc4
ms.date: 12/05/2018
ms.keywords: SLGetSLIDList, SLGetSLIDList function [Security], security.slgetslidlist, slpublic/SLGetSLIDList
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
 - SLGetSLIDList
 - slpublic/SLGetSLIDList
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
 - SLGetSLIDList
---

# SLGetSLIDList function


## -description

Gets a list of <b>SLID</b>s according to the input query ID type and the ID value.

## -parameters

### -param hSLC [in]

Type: <b>HSLC</b>

The handle to the current SLC context.

### -param eQueryIdType [in]

Type: <b><a href="/windows/desktop/api/slpublic/ne-slpublic-slidtype">SLIDTYPE</a></b>

The type of input ID.

### -param pQueryId [in, optional]

Type: <b>const SLID*</b>

A pointer to the input ID.

### -param eReturnIdType [in]

Type: <b><a href="/windows/desktop/api/slpublic/ne-slpublic-slidtype">SLIDTYPE</a></b>

The type of returned IDs.

### -param pnReturnIds [out]

Type: <b>UINT*</b>

A pointer to the number of returned IDs.

### -param ppReturnIds [out]

Type: <b>SLID**</b>

An array of returned IDs.

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
<dt><b>SL_E_VALUE_NOT_FOUND</b></dt>
<dt>0xC004F012</dt>
</dl>
</td>
<td width="60%">
The value for the input key was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_NOT_SUPPORT</b></dt>
<dt>0xC004F016</dt>
</dl>
</td>
<td width="60%">
The request is not supported.

</td>
</tr>
</table>

## -remarks

The following queries combinations are supported.


<table>
<tr>
<th>eQueryIdType</th>
<th>pQueryId</th>
<th>eReturnIdType</th>
<th>Results</th>
</tr>
<tr>
<td>
<b>SL_ID_APPLICATION</b>

</td>
<td>
SLID_ALL

</td>
<td>
<b>SL_ID_APPLICATION</b>

</td>
<td>
Get all installed application IDs.

</td>
</tr>
<tr>
<td>
<b>SL_ID_PRODUCT_SKU</b>

</td>
<td>
SLID_ALL

</td>
<td>
<b>SL_ID_PRODUCT_SKU</b>

</td>
<td>
Get all installed product SKU IDs.

</td>
</tr>
<tr>
<td>
<b>SL_ID_APPLICATION</b>

</td>
<td>
appId

</td>
<td>
<b>SL_ID_PRODUCT_SKU</b>

</td>
<td>
Get SKU IDs according to the input application ID.

</td>
</tr>
<tr>
<td>
<b>SL_ID_PRODUCT_SKU</b>

</td>
<td>
skuId

</td>
<td>
<b>SL_ID_APPLICATION</b>

</td>
<td>
Get application IDs according to the input SKU ID.

</td>
</tr>
<tr>
<td>
<b>SL_ID_PRODUCT_SKU</b>

</td>
<td>
skuId

</td>
<td>
<b>SL_ID_PKEY</b>

</td>
<td>
Get license PKey IDs according to the input SKU ID.

</td>
</tr>
<tr>
<td>
<b>SL_ID_PRODUCT_SKU</b>

</td>
<td>
skuId

</td>
<td>
<b>SL_ID_LICENSE_FILE</b>

</td>
<td>
Get license file Ids according to the input SKU ID.

</td>
</tr>
<tr>
<td>
<b>SL_ID_LICENSE_FILE</b>

</td>
<td>
fileId

</td>
<td>
<b>SL_ID_LICENSE</b>

</td>
<td>
Get license IDs according to the input license file ID.

</td>
</tr>
<tr>
<td>
<b>SL_ID_LICENSE</b>

</td>
<td>
LicenseId

</td>
<td>
<b>SL_ID_LICENSE_FILE</b>

</td>
<td>
Get license file ID according to the input license ID.

</td>
</tr>
<tr>
<td>
<b>SL_ID_LICENSE</b>

</td>
<td>
LicenseId

</td>
<td>
<b>SL_ID_APPLICATION</b>

</td>
<td>
Get union of all application IDs or SKU IDs from all grants of   
			a token activation license. Returns <b>SL_E_NOT_SUPPORTED</b>   
			if the license ID is valid but doesn't refer to a token   
			activation license.

</td>
</tr>
<tr>
<td>
<b>SL_ID_LICENSE</b>

</td>
<td>
LicenseId

</td>
<td>
<b>SL_ID_PRODUCT_SKU</b>

</td>
<td>
Get union of all application IDs or SKU IDs from all grants of   
			a token activation license. Returns <b>SL_E_NOT_SUPPORTED</b>   
			if the license ID is valid but doesn't refer to a token   
			activation license.

</td>
</tr>
</table>