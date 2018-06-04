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

# UrlEscapeSpaces macro


## -description


A macro that converts space characters into their corresponding escape sequence.


## -parameters




### -param pszUrl

TBD


### -param pszEscaped [out]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string containing the string pointed to by <i>pszURL</i>, with space characters converted to their escape sequence.


### -param pcchEscaped [out]

Type: <b>LPDWORD</b>

The number of characters in <i>pszEscaped</i>.


#### - pszURL [in]

Type: <b>LPCTSTR</b>

A pointer to a URL string. If it does not refer to a file, it must include a valid scheme such as "http://".


## -remarks



<b>UrlEscapeSpaces</b> is equivalent to the following: 

				

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
UrlCanonicalize(pszUrl, 
                pszEscaped, 
                pcchEscaped, 
                URL_ESCAPE_SPACES_ONLY | URL_DONT_ESCAPE_EXTRA_INFO )
				</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/70802745-0611-4d37-800e-b50d5ea23426">UrlCanonicalize</a>
 

 

