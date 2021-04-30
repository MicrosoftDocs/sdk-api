---
UID: NF:lmaccess.NetRemoveServiceAccount
title: NetRemoveServiceAccount function (lmaccess.h)
description: Deletes the specified service account from the Active Directory database if the account is a standalone managed service account (sMSA).
helpviewer_keywords: ["NetRemoveServiceAccount","NetRemoveServiceAccount function [Security]","SERVICE_ACCOUNT_FLAG_UNLINK_FROM_HOST_ONLY","lmaccess/NetRemoveServiceAccount","security.netremoveserviceaccount"]
old-location: security\netremoveserviceaccount.htm
tech.root: security
ms.assetid: f67745b7-bdfd-44bc-83e0-2ad24b78e137
ms.date: 12/05/2018
ms.keywords: NetRemoveServiceAccount, NetRemoveServiceAccount function [Security], SERVICE_ACCOUNT_FLAG_UNLINK_FROM_HOST_ONLY, lmaccess/NetRemoveServiceAccount, security.netremoveserviceaccount
req.header: lmaccess.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetRemoveServiceAccount
 - lmaccess/NetRemoveServiceAccount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetRemoveServiceAccount
---

# NetRemoveServiceAccount function


## -description

The <b>NetRemoveServiceAccount</b> function deletes the specified service account from the <a href="/windows/desktop/AD/active-directory-domain-services">Active Directory</a> database if the account is a standalone managed service account (sMSA). For group managed service accounts (gMSAs), this function does not delete the account from the Active Directory database.  The secret stored in the <a href="/windows/desktop/SecGloss/l-gly">Local Security Authority</a> (LSA) is deleted for both sMSAs and gMSAs, and the state is stored in the Netlogon registry store.

This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Logoncli.dll.

## -parameters

### -param ServerName [in, optional]

The value of this parameter must be <b>NULL</b>.

### -param AccountName [in]

The name of the account to be deleted.

### -param Flags [in]

This parameter can have the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICE_ACCOUNT_FLAG_UNLINK_FROM_HOST_ONLY"></a><a id="service_account_flag_unlink_from_host_only"></a><dl>
<dt><b>SERVICE_ACCOUNT_FLAG_UNLINK_FROM_HOST_ONLY</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
For sMSAs, the service account object is unlinked from the local computer and the secret stored in the LSA is deleted. The service account object is not deleted from the Active Directory database. This flag has no meaning for gMSAs.

</td>
</tr>
</table>

## -returns

If the function succeeds, it returns <b>STATUS_SUCCESS</b>.

If the function fails, it returns an error code.

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netaddserviceaccount">NetAddServiceAccount</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netenumerateserviceaccounts">NetEnumerateServiceAccounts</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netisserviceaccount">NetIsServiceAccount</a>