---
UID: NF:wincred.CredUIReadSSOCredW
title: CredUIReadSSOCredW function (wincred.h)
description: The CredUIReadSSOCredW function retrieves the user name for a single logon credential.
helpviewer_keywords: ["CredUIReadSSOCredW","CredUIReadSSOCredW function [Security]","security.creduireadssocredw","wincred/CredUIReadSSOCredW"]
old-location: security\creduireadssocredw.htm
tech.root: security
ms.assetid: 875be45d-ad33-4a51-80ad-8217ca0446dc
ms.date: 12/05/2018
ms.keywords: CredUIReadSSOCredW, CredUIReadSSOCredW function [Security], security.creduireadssocredw, wincred/CredUIReadSSOCredW
req.header: wincred.h
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
req.lib: Credui.lib
req.dll: Credui.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CredUIReadSSOCredW
 - wincred/CredUIReadSSOCredW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Credui.dll
 - Ext-MS-Win-security-credui-l1-1-1.dll
 - AnalogCredUI.dll
api_name:
 - CredUIReadSSOCredW
---

# CredUIReadSSOCredW function


## -description

The <b>CredUIReadSSOCredW</b> function retrieves the user name for a single logon credential.

## -parameters

### -param pszRealm [in]

Pointer to a <b>null</b>-terminated string that specifies the realm. If this parameter is <b>NULL</b>, the default realm is used.

### -param ppszUsername [out]

Pointer to a pointer to a <b>null</b>-terminated string. When you have finished using the string, free <i>ppszUsername</i> by calling the  <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function.

## -returns

The return value is a <b>DWORD</b>. The following table lists the possible values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The credential was not found.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wincred/nf-wincred-creduistoressocredw">CredUIStoreSSOCredW</a>