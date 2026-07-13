---
UID: NS:winhttp._WINHTTP_URL_COMPONENTS
title: URL_COMPONENTS (winhttp.h)
description: The URL_COMPONENTS structure contains the constituent parts of a URL. This structure is used with the WinHttpCrackUrl and WinHttpCreateUrl functions.
helpviewer_keywords: ["*LPURL_COMPONENTS","INTERNET_SCHEME_HTTP","INTERNET_SCHEME_HTTPS","URL_COMPONENTS","URL_COMPONENTS structure [HTTP]","URL_COMPONENTSW","http.url_components","winhttp/URL_COMPONENTS","winhttp_url_components_structure"]
old-location: http\url_components.htm
tech.root: http
ms.assetid: 4d2c6f82-6b61-4a7b-a5d7-560152e25302
ms.date: 12/05/2018
ms.keywords: '*LPURL_COMPONENTS, INTERNET_SCHEME_HTTP, INTERNET_SCHEME_HTTPS, URL_COMPONENTS, URL_COMPONENTS structure [HTTP], URL_COMPONENTSW, http.url_components, winhttp/URL_COMPONENTS, winhttp_url_components_structure'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: URL_COMPONENTS, *LPURL_COMPONENTS
req.redist: WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.
ms.custom: 19H1
f1_keywords:
 - LPURL_COMPONENTS
 - winhttp/LPURL_COMPONENTS
 - URL_COMPONENTS
 - winhttp/URL_COMPONENTS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winhttp.h
api_name:
 - URL_COMPONENTS
---

## -description

The <b>URL_COMPONENTS</b> structure contains the constituent parts of a URL. This structure is used with the 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpcrackurl">WinHttpCrackUrl</a> and 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpcreateurl">WinHttpCreateUrl</a> functions.

## -struct-fields

### -field dwStructSize

Size of this structure, in bytes. Used for version checking. The size of this structure must be set to initialize this structure properly.

### -field lpszScheme

Pointer to a string value that contains the scheme name.

### -field dwSchemeLength

Length of the scheme name, in characters.

### -field nScheme

Internet protocol scheme.  This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INTERNET_SCHEME_HTTP"></a><a id="internet_scheme_http"></a><dl>
<dt><b>INTERNET_SCHEME_HTTP</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The Internet scheme is the HTTP protocol.  See 
<a href="https://www.ietf.org/rfc/rfc2616.txt">RFC 2616</a> for more information.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_SCHEME_HTTPS"></a><a id="internet_scheme_https"></a><dl>
<dt><b>INTERNET_SCHEME_HTTPS</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The Internet scheme, HTTPS, is an HTTP protocol that uses secure transaction semantics.

</td>
</tr>
</table>

### -field lpszHostName

Pointer to a string value that contains the host name.

### -field dwHostNameLength

Length of the host name, in characters.

### -field nPort

Port number.

### -field lpszUserName

Pointer to a string  that contains the user name.

### -field dwUserNameLength

Length of the user name, in characters.

### -field lpszPassword

Pointer to a string  that contains the password.

### -field dwPasswordLength

Length of the password, in characters.

### -field lpszUrlPath

Pointer to a string  that contains the URL path.

### -field dwUrlPathLength

Length of the URL path, in characters.

### -field lpszExtraInfo

Pointer to a string value that contains the extra information, for example, ?something or #something.

### -field dwExtraInfoLength

Unsigned long integer value that contains the length of the extra information, in characters.

## -remarks

For the 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpcrackurl">WinHttpCrackUrl</a> function, if a pointer member and its corresponding length member are both zero, that component of the URL is not returned. If the pointer member is <b>NULL</b> but the length member is not zero, both the pointer and length members are returned. If both pointer and corresponding length members are nonzero, the pointer member points to a buffer where the component is copied. All escape sequences can be removed from a component, depending on the 
<i>dwFlags</i> parameter of 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpcrackurl">WinHttpCrackUrl</a>.

For the 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpcreateurl">WinHttpCreateUrl</a> function, the pointer members should be <b>NULL</b> if the component of the URL is not required. If the corresponding length member is zero, the pointer member is the pointer to a zero-terminated string. If the length member is not zero, it is the string length of the corresponding pointer member.

<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="/windows/desktop/WinHttp/winhttp-start-page">Run-Time Requirements</a> section of the WinHttp start page.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/WinHttp/winhttp-versions">WinHTTP
		  Versions</a>