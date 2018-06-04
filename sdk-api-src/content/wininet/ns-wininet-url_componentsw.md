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

# URL_COMPONENTSW structure


## -description


Contains the constituent parts of a URL. This structure is used with the 
<a href="https://msdn.microsoft.com/30677071-3eb2-4d9c-a0a3-ff11a077f98a">InternetCrackUrl</a> and 
<a href="https://msdn.microsoft.com/b01bb684-0b2f-4c17-ab32-9f83fdd89e69">InternetCreateUrl</a> functions.


## -struct-fields




### -field dwStructSize

Size of this structure, in bytes. 


### -field lpszScheme

Pointer to a string that contains the scheme name. 


### -field dwSchemeLength

Size of the scheme name, in <b>TCHARs</b>. 


### -field nScheme


<a href="https://msdn.microsoft.com/640d0b62-a44f-4115-be27-9976da4bc73a">INTERNET_SCHEME</a> value that indicates the Internet protocol scheme. 


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
<a href="https://msdn.microsoft.com/30677071-3eb2-4d9c-a0a3-ff11a077f98a">InternetCrackUrl</a>, if a pointer member and its corresponding length member are both zero, that component is not returned. If the pointer member is <b>NULL</b> but the length member is not zero, both the pointer and length members are returned. If both pointer and corresponding length members are nonzero, the pointer member points to a buffer where the component is copied. The component can be un-escaped, depending on the 
<i>dwFlags</i> parameter of 
<a href="https://msdn.microsoft.com/30677071-3eb2-4d9c-a0a3-ff11a077f98a">InternetCrackUrl</a>.

For 
<a href="https://msdn.microsoft.com/b01bb684-0b2f-4c17-ab32-9f83fdd89e69">InternetCreateUrl</a>, the pointer members should be <b>NULL</b> if the component is not required. If the corresponding length member is zero, the pointer member is the address of a zero-terminated string. If the length member is not zero, it is the string length of the corresponding pointer member.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/30677071-3eb2-4d9c-a0a3-ff11a077f98a">InternetCrackUrl</a>



<a href="https://msdn.microsoft.com/b01bb684-0b2f-4c17-ab32-9f83fdd89e69">InternetCreateUrl</a>
 

 

