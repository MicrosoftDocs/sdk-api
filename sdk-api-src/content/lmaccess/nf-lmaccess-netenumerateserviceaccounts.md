---
UID: NF:lmaccess.NetEnumerateServiceAccounts
title: NetEnumerateServiceAccounts function (lmaccess.h)
description: Enumerates the standalone managed service accounts (sMSA) on the specified server.
helpviewer_keywords: ["NetEnumerateServiceAccounts","NetEnumerateServiceAccounts function [Security]","lmaccess/NetEnumerateServiceAccounts","security.netenumerateserviceaccounts"]
old-location: security\netenumerateserviceaccounts.htm
tech.root: security
ms.assetid: 048116b6-1bae-4dcc-9bd0-a466c395e5d8
ms.date: 12/05/2018
ms.keywords: NetEnumerateServiceAccounts, NetEnumerateServiceAccounts function [Security], lmaccess/NetEnumerateServiceAccounts, security.netenumerateserviceaccounts
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
 - NetEnumerateServiceAccounts
 - lmaccess/NetEnumerateServiceAccounts
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
 - NetEnumerateServiceAccounts
---

# NetEnumerateServiceAccounts function


## -description

The <b>NetEnumerateServiceAccounts</b> function enumerates the standalone managed service accounts (sMSA) on the specified server. This function only enumerates sMSAs and not group managed service accounts (gMSA).

This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Logoncli.dll.

## -parameters

### -param ServerName [in, optional]

The value of this parameter must be <b>NULL</b>.

### -param Flags [in]

This parameter is reserved. Do not use it.

### -param AccountsCount [out]

The number of elements in the <i>Accounts</i> array.

### -param Accounts [out]

A pointer to an array of the names of the service accounts on the specified server.

When you have finished using the names, free the array by calling the <a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function.

## -returns

If the function succeeds, it returns <b>STATUS_SUCCESS</b>.

If the function fails, it returns an error code.

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netaddserviceaccount">NetAddServiceAccount</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netisserviceaccount">NetIsServiceAccount</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netremoveserviceaccount">NetRemoveServiceAccount</a>