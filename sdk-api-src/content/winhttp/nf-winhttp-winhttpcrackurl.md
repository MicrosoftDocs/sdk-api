---
UID: NF:winhttp.WinHttpCrackUrl
title: WinHttpCrackUrl function (winhttp.h)
description: The WinHttpCrackUrl function separates a URL into its component parts such as host name and path.
helpviewer_keywords: ["ICU_DECODE","ICU_ESCAPE","ICU_REJECT_USERPWD","WinHttpCrackUrl","WinHttpCrackUrl function [WinHTTP]","http.winhttpcrackurl","winhttp.winhttpcrackurl_function","winhttp/WinHttpCrackUrl"]
old-location: http\winhttpcrackurl.htm
tech.root: http
ms.assetid: 656dfe11-2242-4587-aa53-87a280f5df81
ms.date: 12/05/2018
ms.keywords: ICU_DECODE, ICU_ESCAPE, ICU_REJECT_USERPWD, WinHttpCrackUrl, WinHttpCrackUrl function [WinHTTP], http.winhttpcrackurl, winhttp.winhttpcrackurl_function, winhttp/WinHttpCrackUrl
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
 - WinHttpCrackUrl
 - winhttp/WinHttpCrackUrl
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
 - WinHttpCrackUrl
---

# WinHttpCrackUrl function


## -description

The <b>WinHttpCrackUrl</b> function separates a URL into its component parts such as host name and path.

## -parameters

### -param pwszUrl [in]

Pointer to a string that contains the canonical URL to separate. <b>WinHttpCrackUrl</b> does not check this URL for validity or correct format before attempting to crack it.

### -param dwUrlLength [in]

The length of the 
<i>pwszUrl</i> string, in characters. If 
<i>dwUrlLength</i> is set to zero, 
<b>WinHttpCrackUrl</b> assumes that the 
<i>pwszUrl</i> string is <b>null</b> terminated and  determines the length of the 
<i>pwszUrl</i> string based on that assumption.

### -param dwFlags [in]

The flags that control the operation. This parameter can be a combination of one or more of the following flags (values can be bitwise OR'd together). Or, the parameter can be 0, which performs no special operations.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ICU_DECODE"></a><a id="icu_decode"></a><dl>
<dt><b>ICU_DECODE</b></dt>
</dl>
</td>
<td width="60%">
Converts characters that are "escape encoded" (%xx) to their non-escaped form.  This does not decode other encodings, such as UTF-8. This feature can be used only if the user provides buffers in the <a href="/windows/win32/api/winhttp/ns-winhttp-url_components">URL_COMPONENTS</a> structure to copy the components into.



</td>
</tr>
<tr>
<td width="40%"><a id="ICU_ESCAPE"></a><a id="icu_escape"></a><dl>
<dt><b>ICU_ESCAPE</b></dt>
</dl>
</td>
<td width="60%">
Escapes certain characters to their escape sequences (%xx). Characters to be escaped are non-ASCII characters or those ASCII characters that must be escaped to be represented in an HTTP request.  This feature can be used only if the user provides buffers in the 
<a href="/windows/win32/api/winhttp/ns-winhttp-url_components">URL_COMPONENTS</a> structure to copy the components into. 

</td>
</tr>
<tr>
<td width="40%"><a id="ICU_REJECT_USERPWD"></a><a id="icu_reject_userpwd"></a><dl>
<dt><b>ICU_REJECT_USERPWD</b></dt>
</dl>
</td>
<td width="60%">
Rejects URLs as input that contain embedded credentials (either a username, a password, or both). If the function fails because of an invalid URL, then subsequent calls to GetLastError return <b>ERROR_WINHTTP_INVALID_URL</b>.
</td>
</tr>
</table>

### -param lpUrlComponents [in, out]

Pointer to a 
<a href="/windows/win32/api/winhttp/ns-winhttp-url_components">URL_COMPONENTS</a> structure that receives the URL components.

## -returns

Returns <b>TRUE</b> if the function succeeds, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Among the error codes returned are the following.

<table>
<tr>
<th>Error Codes</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INTERNAL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An internal error has occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INVALID_URL</b></dt>
</dl>
</td>
<td width="60%">
The URL is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_UNRECOGNIZED_SCHEME</b></dt>
</dl>
</td>
<td width="60%">
The URL scheme could not be recognized, or is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory was available to complete the requested operation. (Windows error code)

</td>
</tr>
</table>

## -remarks

Even when  WinHTTP is used in asynchronous mode (that is, when <b>WINHTTP_FLAG_ASYNC</b> has been set in <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>), this function operates synchronously. The return value indicates success or failure.  To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The required components are indicated by members of the 
<a href="/windows/win32/api/winhttp/ns-winhttp-url_components">URL_COMPONENTS</a> structure. Each component has a pointer to the value and has a member that stores the length of the stored value. If both the value and the length for a component are equal to zero, that component is not returned. If the pointer to the value of the component is <b>NULL</b> and the value of its corresponding length member is nonzero, the address of the first character of the corresponding component in the 
<i>pwszUrl</i> string is stored in the pointer, and the length of the component is stored in the length member.

If the pointer contains the address of the user-supplied buffer, the length member must contain the size of the buffer. The 
<b>WinHttpCrackUrl</b> function copies the component into the buffer, and the length member is set to the length of the copied component, minus 1 for the trailing string terminator. If a user-supplied buffer is not large enough, <b>WinHttpCrackUrl</b> returns <b>FALSE</b>, and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_INSUFFICIENT_BUFFER</b>.

When _lpszExtraInfo_ is not set or _dwExtraInfoLength_ is left as 0 in _lpUrlComponents_, if _lpszUrlPath_ is set the query and/or fragment component of the URL will be included in that field.

For 
<b>WinHttpCrackUrl</b> to work properly, the size of the 
<a href="/windows/win32/api/winhttp/ns-winhttp-url_components">URL_COMPONENTS</a> structure must be stored in the 
<a href="/windows/win32/api/winhttp/ns-winhttp-url_components">dwStructSize</a> member of that structure.

If the Internet protocol of the URL passed in for 
<i>pwszUrl</i> is not HTTP or HTTPS, then 
<b>WinHttpCrackUrl</b>  returns  <b>FALSE</b> and 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>  indicates  
<a href="/windows/desktop/WinHttp/error-messages">ERROR_WINHTTP_UNRECOGNIZED_SCHEME</a>.

<b>WinHttpCrackUrl</b> does not check the validity or format of a URL before attempting to crack it. As a result, if a string such as ""http://server?Bad=URL"" is passed in, the function returns incorrect results.

<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="/windows/desktop/WinHttp/winhttp-start-page">Run-Time Requirements</a> section of the WinHttp start page.</div>
<div> </div>

#### Examples

This example shows how to break a URL into its components, update a component, then reconstruct the URL.


```cpp
    URL_COMPONENTS urlComp;
    LPCWSTR pwszUrl1 = 
      L"http://search.msn.com/results.asp?RS=CHECKED&FORM=MSNH&v=1&q=wininet";
    DWORD dwUrlLen = 0;

    // Initialize the URL_COMPONENTS structure.
    ZeroMemory(&urlComp, sizeof(urlComp));
    urlComp.dwStructSize = sizeof(urlComp);

    // Set required component lengths to non-zero 
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
        // Change the search information.  
        // New info is the same length.
        urlComp.lpszExtraInfo = L"?RS=CHECKED&FORM=MSNH&v=1&q=winhttp";

        // Obtain the size of the new URL and allocate memory.
        WinHttpCreateUrl( &urlComp, 0, NULL, &dwUrlLen);
        LPWSTR pwszUrl2 = new WCHAR[dwUrlLen];

        // Create a new URL.
        if(!WinHttpCreateUrl( &urlComp, 0, pwszUrl2, &dwUrlLen))
        {
            printf("Error %u in WinHttpCreateUrl.\n", GetLastError());
        }
        else
        {
            // Show both URLs.
            printf("Old URL:  %S\nNew URL:  %S\n", pwszUrl1, pwszUrl2);
        }

        // Free allocated memory.
        delete [] pwszUrl2;
    }

```

## -see-also

<a href="/windows/desktop/WinHttp/about-winhttp">About Microsoft Windows HTTP Services (WinHTTP)</a>



<a href="/windows/desktop/WinHttp/uniform-resource-locators--urls--in-winhttp">Handling Uniform Resource Locators</a>



<a href="/windows/desktop/WinHttp/winhttp-versions">WinHTTP Versions</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpcreateurl">WinHttpCreateUrl</a>