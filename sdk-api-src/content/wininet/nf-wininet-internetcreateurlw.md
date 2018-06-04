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

# InternetCreateUrlW function


## -description


Creates a URL from its component parts.


## -parameters




### -param lpUrlComponents [in]

Pointer to a 
<a href="https://msdn.microsoft.com/faebdd29-f746-486b-b779-cceeecac9163">URL_COMPONENTS</a> structure that contains the components from which to create the URL.


### -param dwFlags [in]

Controls the operation of this function. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>ICU_ESCAPE</dt>
</dl>
</td>
<td width="60%">
Converts all unsafe characters to their corresponding escape sequences in the path string pointed to by the <b>lpszUrlPath</b> member and in <b>lpszExtraInfo</b> the extra-information string pointed to by the member of the <a href="https://msdn.microsoft.com/faebdd29-f746-486b-b779-cceeecac9163">URL_COMPONENTS</a> structure pointed to by the <i>lpUrlComponents</i> parameter.

The Unicode version of <b>InternetCreateUrl</b> will first try to convert using the system code page.  If that fails it falls back to UTF-8.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>ICU_USERNAME</dt>
</dl>
</td>
<td width="60%">
Obsolete — ignored.

</td>
</tr>
</table>
 


### -param lpszUrl [out]

Pointer to a buffer that receives the URL.


### -param lpdwUrlLength [in, out]

Pointer to a variable that specifies the size of the 
URL<i>lpszUrl</i> buffer, in <b>TCHARs</b>. When the function returns, this parameter receives the size of the URL string, excluding the NULL terminator. If 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER, this parameter receives the number of bytes required to hold the created URL.


## -returns



Returns <b>TRUE</b> if the function succeeds, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



When specifying scheme in the <a href="https://msdn.microsoft.com/faebdd29-f746-486b-b779-cceeecac9163">URL_COMPONENTS</a> structure passed to <i>lpUrlComponents</i>, if <i>lpszScheme</i> is not NULL it will be used for the scheme.  If <i>lpszScheme</i> is NULL, the scheme can be specified using the <a href="https://msdn.microsoft.com/640d0b62-a44f-4115-be27-9976da4bc73a">INTERNET_SCHEME</a> enumeration by setting <b>nScheme</b> to the required <b>INTERNET_SCHEME</b> or <b>INTERNET_SCHEME_DEFAULT</b>.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/bb59ada6-f49f-412c-a32c-4fb9495b1222">Handling Uniform Resource Locators</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

