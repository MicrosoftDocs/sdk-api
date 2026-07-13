---
UID: NF:wsdevlicensing.AcquireDeveloperLicense
title: AcquireDeveloperLicense function (wsdevlicensing.h)
description: Acquires a developer license.
helpviewer_keywords: ["AcquireDeveloperLicense","AcquireDeveloperLicense function","devlic.acquiredeveloperlicense","wsdevlicensing/AcquireDeveloperLicense"]
old-location: devlic\acquiredeveloperlicense.htm
tech.root: devlic
ms.assetid: 0F6316B4-3FE2-405E-B8C0-AB371F95BCE1
ms.date: 12/05/2018
ms.keywords: AcquireDeveloperLicense, AcquireDeveloperLicense function, devlic.acquiredeveloperlicense, wsdevlicensing/AcquireDeveloperLicense
req.header: wsdevlicensing.h
req.include-header: 
req.target-type: Windows
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
req.lib: wsclient.lib
req.dll: WSClient.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AcquireDeveloperLicense
 - wsdevlicensing/AcquireDeveloperLicense
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WSClient.dll
api_name:
 - AcquireDeveloperLicense
---

# AcquireDeveloperLicense function


## -description

Acquires a developer license.

## -parameters

### -param hwndParent [in, optional]

The handler to the parent window.

### -param pExpiration [out]

Indicates when the developer license expires.

## -returns

Returns an <a href="/uwp/api/windows.foundation.hresult">HResult structure</a> with any error codes that occurred.

## -remarks

The following is a list of common error codes that this function returns:

<table>
<tr>
<th>Error code</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>The function succeeded.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>One or more arguments are invalid.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>Insufficient memory.</td>
</tr>
<tr>
<td>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</td>
<td>The license was not found.</td>
</tr>
<tr>
<td>HRESULT_FROM_WIN32(ERROR_NOT_AUTHENTICATED)</td>
<td>The call requires authentication.</td>
</tr>
<tr>
<td>HRESULT_FROM_WIN32(ERROR_NETWORK_UNREACHABLE)</td>
<td>The network can’t be reached.</td>
</tr>
<tr>
<td>HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)</td>
<td>The caller doesn’t have access to the resource (license).</td>
</tr>
</table>