---
UID: NF:adshlp.ADsSetLastError
title: ADsSetLastError function (adshlp.h)
description: The ADsSetLastError sets the last-error code value for the calling thread.
helpviewer_keywords: ["ADsSetLastError","ADsSetLastError function [ADSI]","_ds_adssetlasterror","adshlp/ADsSetLastError","adsi.adssetlasterror"]
old-location: adsi\adssetlasterror.htm
tech.root: adsi
ms.assetid: c9433af7-2ca5-492a-9b8e-9dfedb5e4d9d
ms.date: 12/05/2018
ms.keywords: ADsSetLastError, ADsSetLastError function [ADSI], _ds_adssetlasterror, adshlp/ADsSetLastError, adsi.adssetlasterror
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ADsSetLastError
 - adshlp/ADsSetLastError
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Activeds.dll
api_name:
 - ADsSetLastError
---

# ADsSetLastError function


## -description

The <b>ADsSetLastError</b> sets the last-error code value for the calling thread. Directory service providers can use this function to set extended errors. The function saves the error data in a per-thread data structure. <b>ADsSetLastError</b> operates similar to the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> function.

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

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/ADSI/adsi-functions">ADSI Functions</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-adsgetlasterror">ADsGetLastError</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a>