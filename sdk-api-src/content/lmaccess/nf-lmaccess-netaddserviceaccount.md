---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# NetAddServiceAccount function


## -description


The <b>NetAddServiceAccount</b> function creates a standalone managed service account (sMSA) or retrieves the credentials for a group managed service account (gMSA) and stores the account information on the local computer.

This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Logoncli.dll.

<b>Windows Server 2008 R2:  </b>Installing a managed service account by using the PowerShell command line interface cmdlet to call this function fails with error code  0xC0000225 when the value of the <i>AccountName</i> parameter does not match the corresponding <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Security Accounts Manager</a> (SAM) name of the account.


## -parameters




### -param ServerName [in, optional]

The value of this parameter must be <b>NULL</b>.


### -param AccountName [in]

The name of the account to be created.


### -param Password

TBD


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
 


#### - Reserved [in]

This parameter is reserved. Do not use it.


## -returns



If the function succeeds, it returns <b>STATUS_SUCCESS</b>.

If the function fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/048116b6-1bae-4dcc-9bd0-a466c395e5d8">NetEnumerateServiceAccounts</a>



<a href="https://msdn.microsoft.com/975e7c0d-d803-4d78-99ed-d07369341674">NetIsServiceAccount</a>



<a href="https://msdn.microsoft.com/f67745b7-bdfd-44bc-83e0-2ad24b78e137">NetRemoveServiceAccount</a>
 

 

