---
UID: NF:lmaccess.NetIsServiceAccount
title: NetIsServiceAccount function (lmaccess.h)
author: windows-sdk-content
description: Tests whether the specified standalone managed service account (sMSA) or group managed service account (gMSA) exists in the Netlogon store on the specified server.
old-location: security\netisserviceaccount.htm
tech.root: SecMgmt
ms.assetid: 975e7c0d-d803-4d78-99ed-d07369341674
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: NetIsServiceAccount, NetIsServiceAccount function [Security], lmaccess/NetIsServiceAccount, security.netisserviceaccount
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
req.lib: 
req.dll: Netapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetIsServiceAccount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NetIsServiceAccount function


## -description


The <b>NetIsServiceAccount</b> function tests whether the specified standalone managed service account (sMSA) or group managed service account (gMSA) exists in the Netlogon store on the specified server.

This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Logoncli.dll.


## -parameters




### -param ServerName [in, optional]

The value of this parameter must be <b>NULL</b>.


### -param AccountName [in]

The name of the account to be tested.


### -param IsService [out]

<b>TRUE</b> if the specified service account exists on the specified server; otherwise, <b>FALSE</b>.


## -returns



If the function succeeds, it returns <b>STATUS_SUCCESS</b>.

If the function fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/004bd392-8837-4d98-905a-cd19ed02817d">NetAddServiceAccount</a>



<a href="https://msdn.microsoft.com/048116b6-1bae-4dcc-9bd0-a466c395e5d8">NetEnumerateServiceAccounts</a>



<a href="https://msdn.microsoft.com/f67745b7-bdfd-44bc-83e0-2ad24b78e137">NetRemoveServiceAccount</a>
 

 

