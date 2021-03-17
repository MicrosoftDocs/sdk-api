---
UID: NF:wintrust.WintrustGetDefaultForUsage
title: WintrustGetDefaultForUsage function (wintrust.h)
description: Retrieves the default usage identifier and callback information.
helpviewer_keywords: ["DWACTION_ALLOCANDFILL","DWACTION_FREE","WintrustGetDefaultForUsage","WintrustGetDefaultForUsage function [Security]","security.wintrustgetdefaultforusage","wintrust/WintrustGetDefaultForUsage"]
old-location: security\wintrustgetdefaultforusage.htm
tech.root: security
ms.assetid: B2ED5489-792F-4B00-A21E-EE1B1462D1C8
ms.date: 12/05/2018
ms.keywords: DWACTION_ALLOCANDFILL, DWACTION_FREE, WintrustGetDefaultForUsage, WintrustGetDefaultForUsage function [Security], security.wintrustgetdefaultforusage, wintrust/WintrustGetDefaultForUsage
req.header: wintrust.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wintrust.lib
req.dll: Wintrust.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WintrustGetDefaultForUsage
 - wintrust/WintrustGetDefaultForUsage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
api_name:
 - WintrustGetDefaultForUsage
---

# WintrustGetDefaultForUsage function


## -description

The <b>WintrustGetDefaultForUsage</b> function retrieves the default usage identifier and callback information.

## -parameters

### -param dwAction [in]

Action to perform. This can be one of the following values. For more information, see Remarks.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DWACTION_ALLOCANDFILL"></a><a id="dwaction_allocandfill"></a><dl>
<dt><b>DWACTION_ALLOCANDFILL</b></dt>
</dl>
</td>
<td width="60%">
Allocate memory and fill the <a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_provider_defusage">CRYPT_PROVIDER_DEFUSAGE</a> structure pointed to by the <i>psUsage</i> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="DWACTION_FREE"></a><a id="dwaction_free"></a><dl>
<dt><b>DWACTION_FREE</b></dt>
</dl>
</td>
<td width="60%">
Free all memory allocated during  a previous call to this function by specifying <b>DWACTION_ALLOCANDFILL</b> for this parameter.

</td>
</tr>
</table>

### -param pszUsageOID [in]

Pointer to a string that contains the identifier.

### -param psUsage [in, out]

Pointer to a <a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_provider_defusage">CRYPT_PROVIDER_DEFUSAGE</a> structure that contains callback information to be retrieved.

## -returns

The return value is <b>TRUE</b> if the function succeeds; <b>FALSE</b>  if the function fails.   If the function fails, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function  to determine the reason for failure.

## -remarks

Call this function once with the <i>dwAction</i> parameter set to <b>DWACTION_ALLOCANDFILL</b> to allocate memory and fill a <a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_provider_defusage">CRYPT_PROVIDER_DEFUSAGE</a> structure with information. Call this function again with the <i>dwAction</i> parameter set to <b>DWACTION_FREE</b> to free the allocated memory.

The default usage and callback information for a provider is registered by calling the <a href="/windows/desktop/api/wintrust/nf-wintrust-wintrustadddefaultforusage">WintrustAddDefaultForUsage</a> function.

## -see-also

<a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_provider_defusage">CRYPT_PROVIDER_DEFUSAGE</a>



<a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_provider_regdefusage">CRYPT_PROVIDER_REGDEFUSAGE</a>



<a href="/windows/desktop/api/wintrust/nf-wintrust-wintrustadddefaultforusage">WintrustAddDefaultForUsage</a>