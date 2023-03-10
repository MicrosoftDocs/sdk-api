---
UID: NF:winhttp.WinHttpCreateUrl
title: WinHttpCreateUrl function (winhttp.h)
description: Creates a URL from component parts such as the host name and path.
helpviewer_keywords: ["ICU_ESCAPE","ICU_REJECT_USERPWD","WinHttpCreateUrl","WinHttpCreateUrl function [WinHTTP]","http.winhttpcreateurl","winhttp.winhttpcreateurl_function","winhttp/WinHttpCreateUrl"]
old-location: http\winhttpcreateurl.htm
tech.root: http
ms.assetid: 3f0403ea-479a-4764-ae65-d9bbd9233a50
ms.date: 12/05/2018
ms.keywords: ICU_ESCAPE, ICU_REJECT_USERPWD, WinHttpCreateUrl, WinHttpCreateUrl function [WinHTTP], http.winhttpcreateurl, winhttp.winhttpcreateurl_function, winhttp/WinHttpCreateUrl
req.header: winhttp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winhttp.lib
req.dll: Winhttp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.
ms.custom: 19H1
f1_keywords:
 - WinHttpCreateUrl
 - winhttp/WinHttpCreateUrl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winhttp.dll
api_name:
 - WinHttpCreateUrl
---

# WinHttpCreateUrl function


## -description

The <b>WinHttpCreateUrl</b> function creates a URL from component parts such as the host name and path.

## -parameters

### -param lpUrlComponents [in]

Pointer to a 
<a href="/windows/win32/api/winhttp/ns-winhttp-url_components">URL_COMPONENTS</a> structure that contains the components from which to create the URL.

### -param dwFlags [in]

Flags that control the operation of this function. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ICU_ESCAPE"></a><a id="icu_escape"></a><dl>
<dt><b>ICU_ESCAPE</b></dt>
</dl>
</td>
<td width="60%">
Converts all unsafe characters to their corresponding escape sequences in the path string pointed to by the <b>lpszUrlPath</b> member and in <b>lpszExtraInfo</b> the extra-information string pointed to by the member of the <a href="/windows/win32/api/winhttp/ns-winhttp-url_components">URL_COMPONENTS</a> structure pointed to by the <i>lpUrlComponents</i> parameter.



</td>
</tr>
<tr>
<td width="40%"><a id="ICU_REJECT_USERPWD"></a><a id="icu_reject_userpwd"></a><dl>
<dt><b>ICU_REJECT_USERPWD</b></dt>
</dl>
</td>
<td width="60%">
Rejects URLs as input that contains either a username, or a password, or both. If the function fails because of an invalid URL, subsequent calls to GetLastError will return ERROR_WINHTTP_INVALID_URL.



</td>
</tr>
</table>

### -param pwszUrl [out]

Pointer to a character buffer that receives the URL as a wide character (Unicode) string.

### -param pdwUrlLength [in, out]

Pointer to a variable of type unsigned long integer that receives the length of the 
<i>pwszUrl</i> buffer in wide (Unicode) characters. When the function returns, this parameter receives the length of the URL string wide in characters, minus 1 for the terminating character. If 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER, this parameter receives the number of wide characters required to hold the created URL.

## -returns

Returns <b>TRUE</b> if the function succeeds, or <b>FALSE</b> otherwise. To get extended error data, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Among the error codes returned are the following.

<table>
<tr>
<th>Error Code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INTERNAL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An internal error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory available to complete the requested operation. (Windows error code)

</td>
</tr>
</table>

## -remarks

Even when  WinHTTP is used in asynchronous mode, that is, when <b>WINHTTP_FLAG_ASYNC</b> has been set in <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>, this function operates synchronously. The return value indicates success or failure.  To get extended error data, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="/windows/desktop/WinHttp/winhttp-start-page">Run-Time Requirements</a> section of the WinHttp start page.</div>
<div> </div>

#### Examples

The following  example shows how to decompile, or crack, a URL into its subcomponents, update a component, then reconstruct the URL.


```cpp

    URL_COMPONENTS urlComp;
    LPCWSTR pwszUrl1 = 
       L"http://search.msn.com/results.asp?RS=CHECKED&FORM=MSNH&v=1&q=wininet";
    DWORD dwUrlLen = 0;

    // Initialize the URL_COMPONENTS structure.
    ZeroMemory(&urlComp, sizeof(urlComp));
    urlComp.dwStructSize = sizeof(urlComp);

    // Set required component lengths to non-zero, 
    // so that they are cracked.
    urlComp.dwSchemeLength    = (DWORD)-1;
    urlComp.dwHostNameLength  = (DWORD)-1;
    urlComp.dwUrlPathLength   = (DWORD)-1;
    urlComp.dwExtraInfoLength = (DWORD)-1;

    // Crack the URL.
    if (!WinHttpCrackUrl( pwszUrl1, (DWORD)wcslen(pwszUrl1), 0, &urlComp))
    {
        printf("Error %u in WinHttpCrackUrl.\n", GetLastError());
    }
    else
    {
        // Change the search data. New data is the same length.
        urlComp.lpszExtraInfo = L"?RS=CHECKED&FORM=MSNH&v=1&q=winhttp";

        // Obtain the size of the new URL and allocate memory.
        WinHttpCreateUrl( &urlComp, 0, NULL, &dwUrlLen);
        LPWSTR pwszUrl2 = new WCHAR[dwUrlLen];

        // Create a new URL.
        if(!WinHttpCreateUrl( &urlComp, 0, pwszUrl2, &dwUrlLen))
        {
            printf( "Error %u in WinHttpCreateUrl.\n", GetLastError());
        }
        else
        {
            // Show both URLs.
            printf( "Old URL:  %S\nNew URL:  %S\n", pwszUrl1, pwszUrl2);
        }

        // Free allocated memory.
        delete [] pwszUrl2;
    }

```

## -see-also

<a href="/windows/desktop/WinHttp/about-winhttp">About Microsoft Windows HTTP Services (WinHTTP)</a>



<a href="/windows/desktop/WinHttp/uniform-resource-locators--urls--in-winhttp">Handling Uniform Resource Locators</a>



<a href="/windows/desktop/WinHttp/winhttp-versions">WinHTTP Versions</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpcrackurl">WinHttpCrackUrl</a>