---
UID: NF:slpublic.SLGenerateOfflineInstallationIdEx
title: SLGenerateOfflineInstallationIdEx function (slpublic.h)
description: Generates Installation ID (IID).
helpviewer_keywords: ["SLGenerateOfflineInstallationIdEx","SLGenerateOfflineInstallationIdEx function [Security]","security.slgenerateofflineinstallationidex","slpublic/SLGenerateOfflineInstallationIdEx"]
old-location: security\slgenerateofflineinstallationidex.htm
tech.root: security
ms.assetid: a9fd3717-7f1d-4f53-a246-c0542fc2e474
ms.date: 12/05/2018
ms.keywords: SLGenerateOfflineInstallationIdEx, SLGenerateOfflineInstallationIdEx function [Security], security.slgenerateofflineinstallationidex, slpublic/SLGenerateOfflineInstallationIdEx
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
 - SLGenerateOfflineInstallationIdEx
 - slpublic/SLGenerateOfflineInstallationIdEx
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
 - SLGenerateOfflineInstallationIdEx
---

# SLGenerateOfflineInstallationIdEx function


## -description

Generates Installation ID (IID). Users can send the IID to CSR to get the Confirmation ID (CID).

## -parameters

### -param hSLC [in]

Type: <b>HSLC</b>

The handle to the current SLC context.

### -param pProductSkuId [in, optional]

Type: <b>const SLID*</b>

A pointer the product ID.

### -param pActivationInfo [in, optional]

Type: <b>const <a href="/windows/desktop/api/slpublic/ns-slpublic-sl_activation_info_header">SL_ACTIVATION_INFO_HEADER</a>*</b>

A pointer to additional information.

### -param ppwszInstallationId [out]

Type: <b>PWSTR*</b>

The Installation ID string. Once you are finished, call the <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function to      
		free the memory.

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
</table>