---
UID: NF:adshlp.ADsGetLastError
title: ADsGetLastError function
author: windows-sdk-content
description: The ADsGetLastError function retrieves the calling thread's last-error code value.
old-location: adsi\adsgetlasterror.htm
tech.root: ADSI
ms.assetid: 5e9899e9-e51e-4785-812a-f86eac6e2006
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ADsGetLastError, ADsGetLastError function [ADSI], _ds_adsgetlasterror, adshlp/ADsGetLastError, adsi.adsgetlasterror
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
req.dll: Activeds.dll; AdsLdpc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Activeds.dll
 - AdsLdpc.dll
api_name:
 - ADsGetLastError
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ADsGetLastError function


## -description


The <b>ADsGetLastError</b> function retrieves the calling thread's last-error code value.


## -parameters




### -param lpError [out]

Type: <b>LPDWORD</b>

Pointer to the location that receives the error code.


### -param lpErrorBuf [out]

Type: <b>LPWSTR</b>

Pointer to the location that receives the null-terminated Unicode string that describes the error.


### -param dwErrorBufLen [in]

Type: <b>DWORD</b>

Size, in characters, of the <i>lpErrorBuf</i> buffer. If the buffer is too small to receive the error string, the string is truncated, but still null-terminated. A buffer, of at least 256 bytes, is recommended.


### -param lpNameBuf [out]

Type: <b>LPWSTR</b>

Pointer to the location that receives the null-terminated Unicode string that describes the name of the provider that raised the error.


### -param dwNameBufLen [in]

Type: <b>DWORD</b>

Size, in characters, of the <i>lpNameBuf</i> buffer. If the buffer is too small to receive the name of the provider, the string is truncated, but still null-terminated.


## -returns



Type: <b>HRESULT</b>

This method supports standard return values, as well as the following.




## -remarks



ADSI errors fall into two types according to the values of their facility code. The standard ADSI error codes have a facility code value of 0x5 and the extended ADSI error codes assume that of FACILITY_WIN32. The error values of the standard and extended ADSI error codes are of the forms of 0x80005xxx and 0x8007xxxx, respectively. Use the HRESULT_FACILITY(hr) macro to determine the ADSI error type.
   


<div class="alert"><b>Note</b>  The WinNT ADSI provider does not support <b>ADsGetLastError</b>.</div>
<div> </div>
The following code example shows how to get Win32 error codes and their descriptions using <b>ADsGetLastError</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>if (FAILED(hr))
{
    wprintf(L"An error occurred.\n  HRESULT: %x\n",hr);
    // If facility is Win32, get the Win32 error 
    if (HRESULT_FACILITY(hr)==FACILITY_WIN32)
    {
        DWORD dwLastError;
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
        }
    }
}</pre>
</td>
</tr>
</table></span></div>
If hr is 80071392, the code example returns the following.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>An error occurred.
    HRESULT: 80071392
    Error Code: 8305
    Error Text: 00002071: UpdErr: DSID-030502F1, problem 6005 (ENTRY_EXISTS), data 0
    Provider: LDAP Provider</pre>
</td>
</tr>
</table></span></div>
<div class="alert"><b>Note</b>  The WinNT ADSI provider does not support <b>ADsGetLastError</b>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/4f0e90e2-afcc-4cf7-a731-9b38a83ca229">ADSI Functions</a>



<a href="https://msdn.microsoft.com/c9433af7-2ca5-492a-9b8e-9dfedb5e4d9d">ADsSetLastError</a>



<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>
 

 

