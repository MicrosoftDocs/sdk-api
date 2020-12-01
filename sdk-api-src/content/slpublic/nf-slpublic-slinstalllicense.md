---
UID: NF:slpublic.SLInstallLicense
title: SLInstallLicense function (slpublic.h)
description: Stores the specified license and returns a license file ID.
helpviewer_keywords: ["SLInstallLicense","SLInstallLicense function [Security]","security.slinstalllicense","slpublic/SLInstallLicense"]
old-location: security\slinstalllicense.htm
tech.root: security
ms.assetid: 39b14ce1-116b-4469-9e95-8cc4db70171a
ms.date: 12/05/2018
ms.keywords: SLInstallLicense, SLInstallLicense function [Security], security.slinstalllicense, slpublic/SLInstallLicense
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
 - SLInstallLicense
 - slpublic/SLInstallLicense
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
 - SLInstallLicense
---

# SLInstallLicense function


## -description

Stores the specified license and returns a license file ID.

## -parameters

### -param hSLC [in]

Type: <b>HSLC</b>

The handle to the current SLC context.

### -param cbLicenseBlob [in]

Type: <b>UINT</b>

Size of license BLOB.

### -param pbLicenseBlob [in]

Type: <b>const BYTE*</b>

A pointer to the licenses in the BLOB.

### -param pLicenseFileId [out]

Type: <b>SLID*</b>

A pointer to the license file ID.

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
<dt><b>SL_E_INVALID_LICENSE</b></dt>
<dt>0xC004F01F</dt>
</dl>
</td>
<td width="60%">
The license is not valid.

</td>
</tr>
</table>

