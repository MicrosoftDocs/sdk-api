---
UID: NF:slpublic.SLGetInstalledProductKeyIds
title: SLGetInstalledProductKeyIds function (slpublic.h)
description: This function returns a list of product key IDs associated with the specified Product SKU ID.
helpviewer_keywords: ["SLGetInstalledProductKeyIds","SLGetInstalledProductKeyIds function [Security]","security.slgetinstalledproductkeyids","slpublic/SLGetInstalledProductKeyIds"]
old-location: security\slgetinstalledproductkeyids.htm
tech.root: security
ms.assetid: 6d678ffa-ef67-41e6-bafa-bdca418c5f9f
ms.date: 12/05/2018
ms.keywords: SLGetInstalledProductKeyIds, SLGetInstalledProductKeyIds function [Security], security.slgetinstalledproductkeyids, slpublic/SLGetInstalledProductKeyIds
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
 - SLGetInstalledProductKeyIds
 - slpublic/SLGetInstalledProductKeyIds
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
 - SLGetInstalledProductKeyIds
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

