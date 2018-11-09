---
UID: NF:winhttp.WinHttpCrackUrl
title: WinHttpCrackUrl function
author: windows-sdk-content
description: The WinHttpCrackUrl function separates a URL into its component parts such as host name and path.
old-location: http\winhttpcrackurl.htm
tech.root: WinHttp
ms.assetid: 656dfe11-2242-4587-aa53-87a280f5df81
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ICU_DECODE, ICU_ESCAPE, ICU_REJECT_USERPWD, WinHttpCrackUrl, WinHttpCrackUrl function [WinHTTP], http.winhttpcrackurl, winhttp.winhttpcrackurl_function, winhttp/WinHttpCrackUrl
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winhttp.dll
api_name:
 - WinHttpCrackUrl
product: Windows
targetos: Windows
req.typenames: 
req.redist: WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.
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

The flags that control the operation. This parameter can be one of the following values.

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
Converts characters that are "escape encoded" (%xx) to their non-escaped form.  This does not decode other encodings, such as UTF-8. This feature can be used only if the user provides buffers in the <a href="https://msdn.microsoft.com/4d2c6f82-6b61-4a7b-a5d7-560152e25302">URL_COMPONENTS</a> structure to copy the components into.



</td>
</tr>
<tr>
<td width="40%"><a id="ICU_ESCAPE"></a><a id="icu_escape"></a><dl>
<dt><b>ICU_ESCAPE</b></dt>
</dl>
</td>
<td width="60%">
Escapes certain characters to their escape sequences (%xx). Characters to be escaped are non-ASCII characters or those ASCII characters that must be escaped to be represented in an HTTP request.  This feature can be used only if the user provides buffers in the 
<a href="https://msdn.microsoft.com/4d2c6f82-6b61-4a7b-a5d7-560152e25302">URL_COMPONENTS</a> structure to copy the components into. 

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
 


### -param lpUrlComponents [in, out]

Pointer to a 
<a href="https://msdn.microsoft.com/4d2c6f82-6b61-4a7b-a5d7-560152e25302">URL_COMPONENTS</a> structure that receives the URL components. 


## -returns



Returns <b>TRUE</b> if the function succeeds, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Among the error codes returned are the following.

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



Even when  WinHTTP is used in asynchronous mode (that is, when <b>WINHTTP_FLAG_ASYNC</b> has been set in <a href="https://msdn.microsoft.com/34ce8f7d-7cc3-4b38-ba6a-1247f50ebd33">WinHttpOpen</a>), this function operates synchronously. The return value indicates success or failure.  To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The required components are indicated by members of the 
<a href="https://msdn.microsoft.com/4d2c6f82-6b61-4a7b-a5d7-560152e25302">URL_COMPONENTS</a> structure. Each component has a pointer to the value and has a member that stores the length of the stored value. If both the value and the length for a component are equal to zero, that component is not returned. If the pointer to the value of the component is not <b>NULL</b> and the value of its corresponding length member is nonzero, the address of the first character of the corresponding component in the 
<i>pwszUrl</i> string is stored in the pointer, and the length of the component is stored in the length member.

If the pointer contains the address of the user-supplied buffer, the length member must contain the size of the buffer. The 
<b>WinHttpCrackUrl</b> function copies the component into the buffer, and the length member is set to the length of the copied component, minus 1 for the trailing string terminator. If a user-supplied buffer is not large enough, <b>WinHttpCrackUrl</b> returns <b>FALSE</b>, and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_INSUFFICIENT_BUFFER</b>.

For 
<b>WinHttpCrackUrl</b> to work properly, the size of the 
<a href="https://msdn.microsoft.com/4d2c6f82-6b61-4a7b-a5d7-560152e25302">URL_COMPONENTS</a> structure must be stored in the 
<a href="https://msdn.microsoft.com/en-us/library/Aa384078(v=VS.85).aspx">dwStructSize</a> member of that structure.

If the Internet protocol of the URL passed in for 
<i>pwszUrl</i> is not HTTP or HTTPS, then 
<b>WinHttpCrackUrl</b>  returns  <b>FALSE</b> and 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>  indicates  
<a href="https://msdn.microsoft.com/en-us/library/Aa383770(v=VS.85).aspx">ERROR_WINHTTP_UNRECOGNIZED_SCHEME</a>.

<b>WinHttpCrackUrl</b> does not check the validity or format of a URL before attempting to crack it. As a result, if a string such as ""http://server?Bad=URL"" is passed in, the function returns incorrect results.

<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Run-Time Requirements</a> section of the WinHttp start page.</div>
<div> </div>

#### Examples

This example shows how to break a URL into its components, update a component, then reconstruct the URL.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    URL_COMPONENTS urlComp;
    LPCWSTR pwszUrl1 = 
      L"http://search.msn.com/results.asp?RS=CHECKED&amp;FORM=MSNH&amp;v=1&amp;q=wininet";
    DWORD dwUrlLen = 0;

    // Initialize the URL_COMPONENTS structure.
    ZeroMemory(&amp;urlComp, sizeof(urlComp));
    urlComp.dwStructSize = sizeof(urlComp);

    // Set required component lengths to non-zero 
    // so that they are cracked.
    urlComp.dwSchemeLength    = (DWORD)-1;
    urlComp.dwHostNameLength  = (DWORD)-1;
    urlComp.dwUrlPathLength   = (DWORD)-1;
    urlComp.dwExtraInfoLength = (DWORD)-1;

    // Crack the URL.
    if (!WinHttpCrackUrl( pwszUrl1, (DWORD)wcslen(pwszUrl1), 0, &amp;urlComp))
    {
        printf("Error %u in WinHttpCrackUrl.\n", GetLastError());
    }
    else
    {
        // Change the search information.  
        // New info is the same length.
        urlComp.lpszExtraInfo = L"?RS=CHECKED&amp;FORM=MSNH&amp;v=1&amp;q=winhttp";

        // Obtain the size of the new URL and allocate memory.
        WinHttpCreateUrl( &amp;urlComp, 0, NULL, &amp;dwUrlLen);
        LPWSTR pwszUrl2 = new WCHAR[dwUrlLen];

        // Create a new URL.
        if(!WinHttpCreateUrl( &amp;urlComp, 0, pwszUrl2, &amp;dwUrlLen))
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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/8337f699-3ec0-4397-acc2-6dc813f7542d">About Microsoft Windows HTTP Services (WinHTTP)</a>



<a href="https://msdn.microsoft.com/940c414d-274f-475c-a50e-7a0853c3c26b">Handling Uniform Resource Locators</a>



<a href="https://msdn.microsoft.com/b69e5087-7849-4cbc-a97b-204a26fdd044">WinHTTP Versions</a>



<a href="https://msdn.microsoft.com/3f0403ea-479a-4764-ae65-d9bbd9233a50">WinHttpCreateUrl</a>
 

 

