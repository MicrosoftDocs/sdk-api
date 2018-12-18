---
UID: NF:wsdevlicensing.CheckDeveloperLicense
title: CheckDeveloperLicense function
author: windows-sdk-content
description: Checks to see if a developer license exists.
old-location: devlic\checkdeveloperlicense.htm
tech.root: devlic
ms.assetid: 957CBEDC-CF3A-4A65-B0D9-4CEACCAAC344
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CheckDeveloperLicense, CheckDeveloperLicense function, devlic.checkdeveloperlicense, wsdevlicensing/CheckDeveloperLicense
ms.topic: function
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
req.lib: 
req.dll: WSClient.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WSClient.dll
 - Ext-MS-Win-WSClient-devlicense-l1-1-0.dll
 - Ext-MS-Win-WSClient-devlicense-l1-1-1.dll
api_name:
 - CheckDeveloperLicense
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CheckDeveloperLicense function


## -description


Checks to see if a developer license exists.


## -parameters




### -param pExpiration [out]

Indicates when the developer license expires.


## -returns



Returns an <a href="https://msdn.microsoft.com/8613f5d5-3b3b-470c-9ad8-c1941ef429cd">HResult structure</a> with any error codes that occurred.




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
<tr>
<td>SEC_E_CONTEXT_EXPIRED
</td>
<td>License is expired.</td>
</tr>
</table>
 



