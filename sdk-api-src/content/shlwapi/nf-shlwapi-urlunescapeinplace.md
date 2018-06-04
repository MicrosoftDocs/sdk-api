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

# UrlUnescapeInPlace macro


## -description


Converts escape sequences back into ordinary characters and overwrites the original string.


## -parameters




### -param pszUrl

TBD


### -param dwFlags [in]

Type: <b>DWORD</b>

The flags that control which characters are unescaped.



#### URL_DONT_UNESCAPE_EXTRA_INFO

Do not convert the # or ? character, or any characters following them in the string.


#### - pszURL [in, out]

Type: <b>LPTSTR</b>

A pointer to a <b>null</b>-terminated string that contains the URL. The converted string is returned through this parameter.


## -remarks



<b>UrlUnescapeInPlace</b> is equivalent to the following:
				

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
UrlUnescape(pszUrl, NULL, NULL, dwFlags | URL_UNESCAPE_INPLACE)
				</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/5bff5161-3b57-4f12-b126-42eac3f60267">UrlUnescape</a>
 

 

