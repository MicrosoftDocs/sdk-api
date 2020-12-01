---
UID: NF:lmaccess.NetAddServiceAccount
title: NetAddServiceAccount function (lmaccess.h)
description: Creates a standalone managed service account (sMSA) or retrieves the credentials for a group managed service account (gMSA) and stores the account information on the local computer.
helpviewer_keywords: ["NetAddServiceAccount","NetAddServiceAccount function [Security]","SERVICE_ACCOUNT_FLAG_LINK_TO_HOST_ONLY","lmaccess/NetAddServiceAccount","security.netaddserviceaccount"]
old-location: security\netaddserviceaccount.htm
tech.root: security
ms.assetid: 004bd392-8837-4d98-905a-cd19ed02817d
ms.date: 12/05/2018
ms.keywords: NetAddServiceAccount, NetAddServiceAccount function [Security], SERVICE_ACCOUNT_FLAG_LINK_TO_HOST_ONLY, lmaccess/NetAddServiceAccount, security.netaddserviceaccount
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
 - NetAddServiceAccount
 - lmaccess/NetAddServiceAccount
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
 - NetAddServiceAccount
---

# NetAddServiceAccount function


## -description

The <b>NetAddServiceAccount</b> function creates a standalone managed service account (sMSA) or retrieves the credentials for a group managed service account (gMSA) and stores the account information on the local computer.

This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Logoncli.dll.

<b>Windows Server 2008 R2:  </b>Installing a managed service account by using the PowerShell command line interface cmdlet to call this function fails with error code  0xC0000225 when the value of the <i>AccountName</i> parameter does not match the corresponding <a href="/windows/desktop/SecGloss/s-gly">Security Accounts Manager</a> (SAM) name of the account.

## -parameters

### -param ServerName [in, optional]

The value of this parameter must be <b>NULL</b>.

### -param AccountName [in]

The name of the account to be created.

### -param Password [in]

This parameter is reserved. Do not use it.

### -param Flags [in]

This parameter can be the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICE_ACCOUNT_FLAG_LINK_TO_HOST_ONLY"></a><a id="service_account_flag_link_to_host_only"></a><dl>
<dt><b>SERVICE_ACCOUNT_FLAG_LINK_TO_HOST_ONLY</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
No standalone managed service account is created. If a service account with the specified name exists, it is linked to the local computer. This flag is ignored if the account name is an existing gMSA.

</td>
</tr>
</table>

## -returns

If the function succeeds, it returns <b>STATUS_SUCCESS</b>.

If the function fails, it returns an error code.

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netenumerateserviceaccounts">NetEnumerateServiceAccounts</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netisserviceaccount">NetIsServiceAccount</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netremoveserviceaccount">NetRemoveServiceAccount</a>