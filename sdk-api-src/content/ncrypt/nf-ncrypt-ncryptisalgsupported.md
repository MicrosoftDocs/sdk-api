---
UID: NF:ncrypt.NCryptIsAlgSupported
title: NCryptIsAlgSupported function (ncrypt.h)
description: Determines if a CNG key storage provider supports a specific cryptographic algorithm.
helpviewer_keywords: ["NCRYPT_SILENT_FLAG","NCryptIsAlgSupported","NCryptIsAlgSupported function [Security]","ncrypt/NCryptIsAlgSupported","security.ncryptisalgsupported_func"]
old-location: security\ncryptisalgsupported_func.htm
tech.root: security
ms.assetid: 99563293-662f-4478-b8da-8526b832012d
ms.date: 12/05/2018
ms.keywords: NCRYPT_SILENT_FLAG, NCryptIsAlgSupported, NCryptIsAlgSupported function [Security], ncrypt/NCryptIsAlgSupported, security.ncryptisalgsupported_func
req.header: ncrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ncrypt.lib
req.dll: Ncrypt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NCryptIsAlgSupported
 - ncrypt/NCryptIsAlgSupported
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ncrypt.dll
api_name:
 - NCryptIsAlgSupported
---

# NCryptIsAlgSupported function


## -description

The <b>NCryptIsAlgSupported</b> function determines if a CNG key storage provider supports a specific cryptographic algorithm.

## -parameters

### -param hProvider [in]

The handle of the key storage provider. This handle is obtained with the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptopenstorageprovider">NCryptOpenStorageProvider</a> function.

### -param pszAlgId [in]

A pointer to a null-terminated Unicode string that identifies the cryptographic algorithm in question. This can be one of the standard <a href="/windows/desktop/SecCNG/cng-algorithm-identifiers">CNG Algorithm Identifiers</a> or the identifier for another registered algorithm.

### -param dwFlags [in]

Flags that modify function behavior. This can be zero (0) or the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_SILENT_FLAG"></a><a id="ncrypt_silent_flag"></a><dl>
<dt><b>NCRYPT_SILENT_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Requests that the key storage provider (KSP) not display any user interface. If the provider must display the UI to operate, the call fails and the KSP should set the <b>NTE_SILENT_CONTEXT</b> error code as the last error.

</td>
</tr>
</table>

## -returns

Returns a status code that indicates the success or failure of the function.


Possible return codes include, but are not limited to, the following.



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
The provider supports the specified algorithm.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwFlags</i> parameter contains one or more flags that are not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle specified by the <i>hProvider</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The provider does not support the specified algorithm.

</td>
</tr>
</table>

## -remarks

If the provider supports the algorithm, this function returns <b>ERROR_SUCCESS</b>. If the provider does not support the algorithm, and no other errors occurred, this function returns <b>NTE_NOT_SUPPORTED</b>.

A service must not call this function from its <a href="/windows/win32/api/winsvc/nf-winsvc-startservicea">StartService Function</a>. If a service calls this function from its StartService function, a deadlock can occur, and the service may stop responding.