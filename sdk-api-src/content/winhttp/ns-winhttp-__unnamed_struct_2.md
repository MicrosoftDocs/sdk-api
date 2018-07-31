---
UID: NS:winhttp.__unnamed_struct_2
title: URL_COMPONENTS
author: windows-sdk-content
description: The URL_COMPONENTS structure contains the constituent parts of a URL. This structure is used with the WinHttpCrackUrl and WinHttpCreateUrl functions.
old-location: http\url_components.htm
old-project: WinHttp
ms.assetid: 4d2c6f82-6b61-4a7b-a5d7-560152e25302
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*LPURL_COMPONENTS, INTERNET_SCHEME_HTTP, INTERNET_SCHEME_HTTPS, URL_COMPONENTS, URL_COMPONENTS structure [HTTP], URL_COMPONENTSW, http.url_components, winhttp/URL_COMPONENTS, winhttp_url_components_structure"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: URL_COMPONENTS, *LPURL_COMPONENTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winhttp.h
api_name:
 - URL_COMPONENTS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# URL_COMPONENTS structure


## -description


The <b>URL_COMPONENTS</b> structure contains the constituent parts of a URL. This structure is used with the 
<a href="https://msdn.microsoft.com/656dfe11-2242-4587-aa53-87a280f5df81">WinHttpCrackUrl</a> and 
<a href="https://msdn.microsoft.com/3f0403ea-479a-4764-ae65-d9bbd9233a50">WinHttpCreateUrl</a> functions.


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
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84048">RFC 2616</a> for more information.

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
<a href="https://msdn.microsoft.com/656dfe11-2242-4587-aa53-87a280f5df81">WinHttpCrackUrl</a> function, if a pointer member and its corresponding length member are both zero, that component of the URL is not returned. If the pointer member is <b>NULL</b> but the length member is not zero, both the pointer and length members are returned. If both pointer and corresponding length members are nonzero, the pointer member points to a buffer where the component is copied. All escape sequences can be removed from a component, depending on the 
<i>dwFlags</i> parameter of 
<a href="https://msdn.microsoft.com/656dfe11-2242-4587-aa53-87a280f5df81">WinHttpCrackUrl</a>.

For the 
<a href="https://msdn.microsoft.com/3f0403ea-479a-4764-ae65-d9bbd9233a50">WinHttpCreateUrl</a> function, the pointer members should be <b>NULL</b> if the component of the URL is not required. If the corresponding length member is zero, the pointer member is the pointer to a zero-terminated string. If the length member is not zero, it is the string length of the corresponding pointer member.

<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Run-Time Requirements</a> section of the WinHttp start page.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/b69e5087-7849-4cbc-a97b-204a26fdd044">WinHTTP
		  Versions</a>
 

 

