---
UID: NS:wininet.URL_COMPONENTSW
title: URL_COMPONENTSW (wininet.h)
description: Contains the constituent parts of a URL. This structure is used with the InternetCrackUrl and InternetCreateUrl functions. (Unicode)
helpviewer_keywords: ["*LPURL_COMPONENTSW","LPURL_COMPONENTS","LPURL_COMPONENTS structure pointer [WinINet]","URL_COMPONENTS","URL_COMPONENTS structure [WinINet]","URL_COMPONENTSA","URL_COMPONENTSW","_inet_url_components_structure","wininet.url_components","wininet/LPURL_COMPONENTS","wininet/URL_COMPONENTS","wininet/URL_COMPONENTSA","wininet/URL_COMPONENTSW"]
old-location: wininet\url_components.htm
tech.root: wininet
ms.assetid: faebdd29-f746-486b-b779-cceeecac9163
ms.date: 12/05/2018
ms.keywords: '*LPURL_COMPONENTSW, LPURL_COMPONENTS, LPURL_COMPONENTS structure pointer [WinINet], URL_COMPONENTS, URL_COMPONENTS structure [WinINet], URL_COMPONENTSA, URL_COMPONENTSW, _inet_url_components_structure, wininet.url_components, wininet/LPURL_COMPONENTS, wininet/URL_COMPONENTS, wininet/URL_COMPONENTSA, wininet/URL_COMPONENTSW'
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: URL_COMPONENTSW (Unicode) and URL_COMPONENTSA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: URL_COMPONENTSW, *LPURL_COMPONENTSW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPURL_COMPONENTSW
 - wininet/LPURL_COMPONENTSW
 - URL_COMPONENTSW
 - wininet/URL_COMPONENTSW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wininet.h
api_name:
 - URL_COMPONENTS
 - URL_COMPONENTSA
 - URL_COMPONENTSW
---

# URL_COMPONENTSW structure


## -description

Contains the constituent parts of a URL. This structure is used with the 
<a href="/windows/desktop/api/wininet/nf-wininet-internetcrackurla">InternetCrackUrl</a> and 
<a href="/windows/desktop/api/wininet/nf-wininet-internetcreateurla">InternetCreateUrl</a> functions.

## -struct-fields

### -field dwStructSize

Size of this structure, in bytes.

### -field lpszScheme

Pointer to a string that contains the scheme name.

### -field dwSchemeLength

Size of the scheme name, in <b>TCHARs</b>.

### -field nScheme

<a href="/windows/desktop/api/wininet/ne-wininet-internet_scheme">INTERNET_SCHEME</a> value that indicates the Internet protocol scheme.

### -field lpszHostName

Pointer to a string that contains the host name.

### -field dwHostNameLength

Size of the host name, in <b>TCHARs</b>.

### -field nPort

Converted port number.

### -field lpszUserName

Pointer to a string value that contains the user name.

### -field dwUserNameLength

Size of the user name, in <b>TCHARs</b>.

### -field lpszPassword

Pointer to a string that contains the password.

### -field dwPasswordLength

Size of the password, in <b>TCHARs</b>.

### -field lpszUrlPath

Pointer to a string that contains the URL path.

### -field dwUrlPathLength

Size of the URL path, in <b>TCHARs</b>.

### -field lpszExtraInfo

Pointer to a string that contains the extra information (for example, ?something or #something).

### -field dwExtraInfoLength

Size of the extra information, in <b>TCHARs</b>.

## -remarks

For 
<a href="/windows/desktop/api/wininet/nf-wininet-internetcrackurla">InternetCrackUrl</a>, if a pointer member and its corresponding length member are both zero, that component is not returned. If the pointer member is <b>NULL</b> but the length member is not zero, both the pointer and length members are returned. If both pointer and corresponding length members are nonzero, the pointer member points to a buffer where the component is copied. The component can be un-escaped, depending on the 
<i>dwFlags</i> parameter of 
<a href="/windows/desktop/api/wininet/nf-wininet-internetcrackurla">InternetCrackUrl</a>.

For 
<a href="/windows/desktop/api/wininet/nf-wininet-internetcreateurla">InternetCreateUrl</a>, the pointer members should be <b>NULL</b> if the component is not required. If the corresponding length member is zero, the pointer member is the address of a zero-terminated string. If the length member is not zero, it is the string length of the corresponding pointer member.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines URL_COMPONENTS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wininet/nf-wininet-internetcrackurla">InternetCrackUrl</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetcreateurla">InternetCreateUrl</a>

