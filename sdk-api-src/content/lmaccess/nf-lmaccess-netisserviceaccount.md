---
UID: NF:lmaccess.NetIsServiceAccount
title: NetIsServiceAccount function (lmaccess.h)
description: Tests whether the specified standalone managed service account (sMSA) or group managed service account (gMSA) exists in the Netlogon store on the specified server.
helpviewer_keywords: ["NetIsServiceAccount","NetIsServiceAccount function [Security]","lmaccess/NetIsServiceAccount","security.netisserviceaccount"]
old-location: security\netisserviceaccount.htm
tech.root: security
ms.assetid: 975e7c0d-d803-4d78-99ed-d07369341674
ms.date: 12/05/2018
ms.keywords: NetIsServiceAccount, NetIsServiceAccount function [Security], lmaccess/NetIsServiceAccount, security.netisserviceaccount
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
 - NetIsServiceAccount
 - lmaccess/NetIsServiceAccount
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
 - NetIsServiceAccount
---

# NetIsServiceAccount function


## -description

The <b>NetIsServiceAccount</b> function tests whether the specified standalone managed service account (sMSA) or group managed service account (gMSA) exists in the Netlogon store on the specified server.

This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Logoncli.dll.

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

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netaddserviceaccount">NetAddServiceAccount</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netenumerateserviceaccounts">NetEnumerateServiceAccounts</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netremoveserviceaccount">NetRemoveServiceAccount</a>