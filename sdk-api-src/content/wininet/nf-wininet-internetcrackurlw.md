---
UID: NF:wininet.InternetCrackUrlW
title: InternetCrackUrlW function (wininet.h)
author: windows-sdk-content
description: Cracks a URL into its component parts.
old-location: wininet\internetcrackurl.htm
tech.root: wininet
ms.assetid: 30677071-3eb2-4d9c-a0a3-ff11a077f98a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICU_DECODE, ICU_ESCAPE, InternetCrackUrl, InternetCrackUrl function [WinINet], InternetCrackUrlA, InternetCrackUrlW, _inet_internetcrackurl_function, wininet.internetcrackurl, wininet/InternetCrackUrl, wininet/InternetCrackUrlA, wininet/InternetCrackUrlW
ms.topic: function
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InternetCrackUrlW (Unicode) and InternetCrackUrlA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - InternetCrackUrl
 - InternetCrackUrlA
 - InternetCrackUrlW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# InternetCrackUrlW function


## -description


Cracks a URL into its component parts.


## -parameters




### -param lpszUrl [in]

Pointer to a string that contains the canonical URL to be cracked.


### -param dwUrlLength [in]

Size of the 
<i>lpszUrl</i> string, in <b>TCHARs</b>, or zero if 
<i>lpszUrl</i> is an ASCIIZ string.


### -param dwFlags [in]

Controls the operation. This parameter can be one of the following values.

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
Converts encoded characters back to their normal form. This can be used only if the user provides buffers in the 
<a href="https://msdn.microsoft.com/faebdd29-f746-486b-b779-cceeecac9163">URL_COMPONENTS</a> structure to copy the components into.

</td>
</tr>
<tr>
<td width="40%"><a id="ICU_ESCAPE"></a><a id="icu_escape"></a><dl>
<dt><b>ICU_ESCAPE</b></dt>
</dl>
</td>
<td width="60%">
Converts all escape sequences (%xx) to their corresponding characters. This can be used only if the user provides buffers in the 
<a href="https://msdn.microsoft.com/faebdd29-f746-486b-b779-cceeecac9163">URL_COMPONENTS</a> structure to copy the components into.

</td>
</tr>
</table>
 


### -param lpUrlComponents [in, out]

Pointer to a 
<a href="https://msdn.microsoft.com/faebdd29-f746-486b-b779-cceeecac9163">URL_COMPONENTS</a> structure that receives the URL components.


## -returns



Returns <b>TRUE</b> if the function succeeds, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The required components are indicated by members of the 
<a href="https://msdn.microsoft.com/faebdd29-f746-486b-b779-cceeecac9163">URL_COMPONENTS</a> structure. Each component has a pointer to the value and has a member that stores the length of the stored value. If both the value and the length for a component are equal to zero, that component is not returned. <b>Windows Vista and later.:  </b>If the pointer to the value of the component is <b>NULL</b> and the value of its corresponding length member is nonzero, the address of the first character of the corresponding component in the 
<i>lpszUrl</i> string is stored in the pointer, and the length of the component is stored in the length member.



If the pointer contains the address of the user-supplied buffer, the length member must contain the size of the buffer. 
<b>InternetCrackUrl</b> copies the component into the buffer, and the length member is set to the length of the copied component, minus 1 for the trailing string terminator.

For 
<b>InternetCrackUrl</b> to work properly, the size of the 
<a href="https://msdn.microsoft.com/faebdd29-f746-486b-b779-cceeecac9163">URL_COMPONENTS</a> structure, in bytes, must be stored in the 
<b>dwStructSize</b> member.

<b>Note</b>  Do not use <b>InternetCrackUrl</b> on "file://" URLs that contain spaces, because  the value returned in the <b>dwUrlPathLength</b> member of the <a href="https://msdn.microsoft.com/faebdd29-f746-486b-b779-cceeecac9163">URL_COMPONENTS</a> structure pointed to by <i>lpUrlComponents</i> is too large. This is only the case, however, with "file://" URLs that contain space characters.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/fb44d7bd-7868-4c53-aa4b-608d79c5bc7c">FtpOpenFile</a>



<a href="https://msdn.microsoft.com/bb59ada6-f49f-412c-a32c-4fb9495b1222">Handling Uniform Resource Locators</a>



<a href="https://msdn.microsoft.com/52b57e3c-3cfe-40bc-b87b-90cf39c5c38d">InternetCloseHandle</a>



<a href="https://msdn.microsoft.com/7c53e399-b8a5-4cc0-9ef6-88d9a525d87f">InternetFindNextFile</a>



<a href="https://msdn.microsoft.com/fe15627b-c77b-45c0-8ff6-02faa8512b57">InternetSetStatusCallback</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

