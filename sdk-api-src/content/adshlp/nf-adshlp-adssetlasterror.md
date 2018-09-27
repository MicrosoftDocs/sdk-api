---
UID: NF:adshlp.ADsSetLastError
title: ADsSetLastError function
author: windows-sdk-content
description: The ADsSetLastError sets the last-error code value for the calling thread.
old-location: adsi\adssetlasterror.htm
tech.root: ADSI
ms.assetid: c9433af7-2ca5-492a-9b8e-9dfedb5e4d9d
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ADsSetLastError, ADsSetLastError function [ADSI], _ds_adssetlasterror, adshlp/ADsSetLastError, adsi.adssetlasterror
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: adshlp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Activeds.lib
req.dll: Activeds.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Activeds.dll
api_name:
 - ADsSetLastError
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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


```cpp
ADsSetLastError(HRESULT_FROM_WIN32(ERROR_DS_OPERATIONS_ERROR),
                L"ERROR_DS_OPERATIONS_ERROR",
                L"LDAP Provider");
```


The user can use the following code example to examine this operation code.


```cpp
DWORD dwLastError;
WCHAR szErrorBuf[MAX_PATH];
WCHAR szNameBuf[MAX_PATH];
// Get extended error value.
HRESULT hr_return =S_OK;
hr_return = ADsGetLastError( &dwLastError,
                               szErrorBuf,
                               MAX_PATH,
                               szNameBuf,
                               MAX_PATH);
if (SUCCEEDED(hr_return))
{
    wprintf(L"Error Code: %d\n Error Text: %ws\n Provider: %ws\n", dwLastError, szErrorBuf, szNameBuf);
}
```


The previous code example produces the following output for the operations error code set above.


```cpp
Error value: 80072020
Error Text: ERROR_DS_OPERATIONS_ERROR
Provider: LDAP Provider
```


If you use <b>ERROR_DS_OPERATIONS_ERROR</b> without invoking the HRESULT_FROM_WIN32 macro when setting the error, the following output is returned.


```cpp
Error value: 2020
Error Text: ERROR_DS_OPERATIONS_ERROR
Provider: LDAP Provider
```





## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/4f0e90e2-afcc-4cf7-a731-9b38a83ca229">ADSI Functions</a>



<a href="https://msdn.microsoft.com/5e9899e9-e51e-4785-812a-f86eac6e2006">ADsGetLastError</a>



<a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a>
 

 

