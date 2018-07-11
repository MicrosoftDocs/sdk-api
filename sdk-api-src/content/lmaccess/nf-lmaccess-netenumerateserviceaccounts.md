---
UID: NF:lmaccess.NetEnumerateServiceAccounts
title: NetEnumerateServiceAccounts function
author: windows-sdk-content
description: Enumerates the standalone managed service accounts (sMSA) on the specified server.
old-location: security\netenumerateserviceaccounts.htm
old-project: secmgmt
ms.assetid: 048116b6-1bae-4dcc-9bd0-a466c395e5d8
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: NetEnumerateServiceAccounts, NetEnumerateServiceAccounts function [Security], lmaccess/NetEnumerateServiceAccounts, security.netenumerateserviceaccounts
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
 - NetEnumerateServiceAccounts
product: Windows
targetos: Windows
req.lib: 
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# NetEnumerateServiceAccounts function


## -description


The <b>NetEnumerateServiceAccounts</b> function enumerates the standalone managed service accounts (sMSA) on the specified server. This function only enumerates sMSAs and not group managed service accounts (gMSA).

This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Logoncli.dll.


## -parameters




### -param ServerName [in, optional]

The value of this parameter must be <b>NULL</b>.


### -param Flags [in]

This parameter is reserved. Do not use it.


### -param AccountsCount [out]

The number of elements in the <i>Accounts</i> array.


### -param Accounts [out]

A pointer to an array of the names of the service accounts on the specified server.

When you have finished using the names, free the array by calling the <a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a> function.


## -returns



If the function succeeds, it returns <b>STATUS_SUCCESS</b>.

If the function fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/004bd392-8837-4d98-905a-cd19ed02817d">NetAddServiceAccount</a>



<a href="https://msdn.microsoft.com/975e7c0d-d803-4d78-99ed-d07369341674">NetIsServiceAccount</a>



<a href="https://msdn.microsoft.com/f67745b7-bdfd-44bc-83e0-2ad24b78e137">NetRemoveServiceAccount</a>
 

 

