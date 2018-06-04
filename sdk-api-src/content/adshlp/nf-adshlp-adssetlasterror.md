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

# ADsSetLastError function


## -description


The <b>ADsSetLastError</b> sets the last-error code value for the calling thread. Directory service providers can use this function to set extended errors. The function saves the error data in a per-thread data structure. <b>ADsSetLastError</b> operates similar to the <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> function.


## -parameters




### -param dwErr [in]

Type: <b>DWORD</b>

The error code that occurred. If this is an error defined by Windows, <i>pszError</i> is ignored. If this is ERROR_EXTENDED_ERROR, it indicates the provider has a network-specific error to report.


### -param pszError [in]

Type: <b>LPWSTR</b>

The null-terminated Unicode string that describes the network-specific error.


### -param pszProvider [in]

Type: <b>LPWSTR</b>

The null-terminated Unicode string that names the ADSI provider that raised the error.


## -returns



This function does not return a value.




## -remarks



In a custom implementation of an ADSI provider, for example, an LDAP provider, you can set an operation error message as follows.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>ADsSetLastError(HRESULT_FROM_WIN32(ERROR_DS_OPERATIONS_ERROR),
                L"ERROR_DS_OPERATIONS_ERROR",
                L"LDAP Provider");</pre>
</td>
</tr>
</table></span></div>
The user can use the following code example to examine this operation code.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>DWORD dwLastError;
WCHAR szErrorBuf[MAX_PATH];
WCHAR szNameBuf[MAX_PATH];
// Get extended error value.
HRESULT hr_return =S_OK;
hr_return = ADsGetLastError( &amp;dwLastError,
                               szErrorBuf,
                               MAX_PATH,
                               szNameBuf,
                               MAX_PATH);
if (SUCCEEDED(hr_return))
{
    wprintf(L"Error Code: %d\n Error Text: %ws\n Provider: %ws\n", dwLastError, szErrorBuf, szNameBuf);
}</pre>
</td>
</tr>
</table></span></div>
The previous code example produces the following output for the operations error code set above.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>Error value: 80072020
Error Text: ERROR_DS_OPERATIONS_ERROR
Provider: LDAP Provider</pre>
</td>
</tr>
</table></span></div>
If you use <b>ERROR_DS_OPERATIONS_ERROR</b> without invoking the HRESULT_FROM_WIN32 macro when setting the error, the following output is returned.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>Error value: 2020
Error Text: ERROR_DS_OPERATIONS_ERROR
Provider: LDAP Provider</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/4f0e90e2-afcc-4cf7-a731-9b38a83ca229">ADSI Functions</a>



<a href="https://msdn.microsoft.com/5e9899e9-e51e-4785-812a-f86eac6e2006">ADsGetLastError</a>



<a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a>
 

 

