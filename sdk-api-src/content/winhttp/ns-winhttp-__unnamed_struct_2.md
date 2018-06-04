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
 

 

