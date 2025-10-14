---
UID: NF:mscat.CryptCATPersistStore
title: CryptCATPersistStore function (mscat.h)
description: Saves the information in the specified catalog store to an unsigned catalog file.
helpviewer_keywords: ["CryptCATPersistStore","CryptCATPersistStore function [Security]","mscat/CryptCATPersistStore","security.cryptcatpersiststore"]
old-location: security\cryptcatpersiststore.htm
tech.root: security
ms.assetid: 2a564b0e-fcc6-4702-8173-d18df7064e53
ms.date: 12/05/2018
ms.keywords: CryptCATPersistStore, CryptCATPersistStore function [Security], mscat/CryptCATPersistStore, security.cryptcatpersiststore
req.header: mscat.h
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
 - CryptCATPersistStore
 - mscat/CryptCATPersistStore
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
 - CryptCATPersistStore
---

# CryptCATPersistStore function


## -description

<p class="CCE_Message">[The  <b>CryptCATPersistStore</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATPersistStore</b> function saves the information in the specified catalog store to an unsigned catalog file.

## -parameters

### -param hCatalog [in]

A handle to the catalog obtained from <a href="/windows/desktop/api/mscat/nf-mscat-cryptcathandlefromstore">CryptCATHandleFromStore</a> or <a href="/windows/desktop/api/mscat/nf-mscat-cryptcatopen">CryptCATOpen</a> function.   Beginning with Windows 8 you must use only <b>CryptCATOpen</b> to retrieve a handle.

## -returns

The return value is <b>TRUE</b> if the function succeeds; otherwise, <b>FALSE</b>.


If this function returns <b>FALSE</b>, additional error information can be obtained by calling the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function. <b>GetLastError</b> will return the following error code.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Beginning with Windows 8 and Windows Server 2012, you must retrieve a handle by calling the  <a href="/windows/desktop/api/mscat/nf-mscat-cryptcatopen">CryptCATOpen</a> function with the <i>dwPublicVersion</i> parameter set to 0x100 or 0x200. For more information, see Remarks.

</td>
</tr>
</table>

## -remarks

The [CRYPTCATSTORE](/windows/desktop/api/mscat/ns-mscat-cryptcatstore)  structure must be initialized before you call <b>CryptCATPersistStore</b>.

Beginning with Windows 8 and Windows Server 2012, the following changes apply to this function:

<ul>
<li>If <a href="/windows/desktop/api/mscat/nf-mscat-cryptcatopen">CryptCATOpen</a> was called with a <i>dwPublicVersion</i> parameter of 0x200, the catalog is written by using the v2 format.</li>
<li>If <a href="/windows/desktop/api/mscat/nf-mscat-cryptcatopen">CryptCATOpen</a> was called with a <i>dwPublicVersion</i> parameter of 0x100, the catalog is written by using the v1 format.</li>
<li>If <a href="/windows/desktop/api/mscat/nf-mscat-cryptcatopen">CryptCATOpen</a> was called with a <i>dwPublicVersion</i> parameter other than 0x200 or 0x100, the <b>CryptCATPersistStore</b> function returns <b>FALSE</b> and the error code is set to <b>ERROR_NOT_SUPPORTED</b>.</li>
</ul>