---
UID: NF:lmaccess.NetRemoveServiceAccount
title: NetRemoveServiceAccount function
author: windows-sdk-content
description: Deletes the specified service account from the Active Directory database if the account is a standalone managed service account (sMSA).
old-location: security\netremoveserviceaccount.htm
old-project: secmgmt
ms.assetid: f67745b7-bdfd-44bc-83e0-2ad24b78e137
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: NetRemoveServiceAccount, NetRemoveServiceAccount function [Security], SERVICE_ACCOUNT_FLAG_UNLINK_FROM_HOST_ONLY, lmaccess/NetRemoveServiceAccount, security.netremoveserviceaccount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: lmaccess.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MSA_INFO_STATE, *PMSA_INFO_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetRemoveServiceAccount
product: Windows
targetos: Windows
req.lib: 
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# NetRemoveServiceAccount function


## -description


The <b>NetRemoveServiceAccount</b> function deletes the specified service account from the <a href="https://msdn.microsoft.com/9fc78c72-c59c-4c4d-ace5-00a431645c4b">Active Directory</a> database if the account is a standalone managed service account (sMSA). For group managed service accounts (gMSAs), this function does not delete the account from the Active Directory database.  The secret stored in the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> (LSA) is deleted for both sMSAs and gMSAs, and the state is stored in the Netlogon registry store.

This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Logoncli.dll.


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




<a href="https://msdn.microsoft.com/004bd392-8837-4d98-905a-cd19ed02817d">NetAddServiceAccount</a>



<a href="https://msdn.microsoft.com/048116b6-1bae-4dcc-9bd0-a466c395e5d8">NetEnumerateServiceAccounts</a>



<a href="https://msdn.microsoft.com/975e7c0d-d803-4d78-99ed-d07369341674">NetIsServiceAccount</a>
 

 

