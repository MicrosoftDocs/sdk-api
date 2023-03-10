---
UID: NF:slpublic.SLUninstallLicense
title: SLUninstallLicense function (slpublic.h)
description: Uninstalls the license specified by the license file ID and target user option.
helpviewer_keywords: ["SLUninstallLicense","SLUninstallLicense function [Security]","security.sluninstalllicense","slpublic/SLUninstallLicense"]
old-location: security\sluninstalllicense.htm
tech.root: security
ms.assetid: 1f79a26e-7605-46ad-9854-e90e73320184
ms.date: 12/05/2018
ms.keywords: SLUninstallLicense, SLUninstallLicense function [Security], security.sluninstalllicense, slpublic/SLUninstallLicense
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
 - SLUninstallLicense
 - slpublic/SLUninstallLicense
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
 - SLUninstallLicense
---

# SLUninstallLicense function


## -description

Uninstalls the license specified by the license file ID and target      
	user option.

## -parameters

### -param hSLC [in]

Type: <b>HSLC</b>

The handle to the current SLC context.

### -param pLicenseFileId [in]

Type: <b>const SLID*</b>

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
Access denied (API requires admin privileges)

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
<dt><b>SL_E_LICENSE_FILE_NOT_INSTALLED</b></dt>
<dt>0xC004F011</dt>
</dl>
</td>
<td width="60%">
The license file is not installed.

</td>
</tr>
</table>

