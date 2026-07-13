---
UID: NF:wininet.InternetCrackUrlA
title: InternetCrackUrlA function (wininet.h)
description: Cracks a URL into its component parts. (ANSI)
helpviewer_keywords: ["ICU_DECODE", "ICU_ESCAPE", "InternetCrackUrlA", "wininet/InternetCrackUrlA"]
old-location: wininet\internetcrackurl.htm
tech.root: wininet
ms.assetid: 30677071-3eb2-4d9c-a0a3-ff11a077f98a
ms.date: 12/05/2018
ms.keywords: ICU_DECODE, ICU_ESCAPE, InternetCrackUrl, InternetCrackUrl function [WinINet], InternetCrackUrlA, InternetCrackUrlW, _inet_internetcrackurl_function, wininet.internetcrackurl, wininet/InternetCrackUrl, wininet/InternetCrackUrlA, wininet/InternetCrackUrlW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InternetCrackUrlA
 - wininet/InternetCrackUrlA
dev_langs:
 - c++
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
---

# InternetCrackUrlA function


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
<a href="/windows/desktop/api/wininet/ns-wininet-url_componentsa">URL_COMPONENTS</a> structure to copy the components into.

</td>
</tr>
<tr>
<td width="40%"><a id="ICU_ESCAPE"></a><a id="icu_escape"></a><dl>
<dt><b>ICU_ESCAPE</b></dt>
</dl>
</td>
<td width="60%">
Converts all escape sequences (%xx) to their corresponding characters. This can be used only if the user provides buffers in the 
<a href="/windows/desktop/api/wininet/ns-wininet-url_componentsa">URL_COMPONENTS</a> structure to copy the components into.

</td>
</tr>
</table>

### -param lpUrlComponents [in, out]

Pointer to a 
<a href="/windows/desktop/api/wininet/ns-wininet-url_componentsa">URL_COMPONENTS</a> structure that receives the URL components.

## -returns

Returns <b>TRUE</b> if the function succeeds, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The required components are indicated by members of the 
<a href="/windows/desktop/api/wininet/ns-wininet-url_componentsa">URL_COMPONENTS</a> structure. Each component has a pointer to the value and has a member that stores the length of the stored value. If both the value and the length for a component are equal to zero, that component is not returned. <b>Windows Vista and later.:  </b>If the pointer to the value of the component is <b>NULL</b> and the value of its corresponding length member is nonzero, the address of the first character of the corresponding component in the 
<i>lpszUrl</i> string is stored in the pointer, and the length of the component is stored in the length member.



If the pointer contains the address of the user-supplied buffer, the length member must contain the size of the buffer. 
<b>InternetCrackUrl</b> copies the component into the buffer, and the length member is set to the length of the copied component, minus 1 for the trailing string terminator.

For 
<b>InternetCrackUrl</b> to work properly, the size of the 
<a href="/windows/desktop/api/wininet/ns-wininet-url_componentsa">URL_COMPONENTS</a> structure, in bytes, must be stored in the 
<b>dwStructSize</b> member.

<b>Note</b>  Do not use <b>InternetCrackUrl</b> on "file://" URLs that contain spaces, because  the value returned in the <b>dwUrlPathLength</b> member of the <a href="/windows/desktop/api/wininet/ns-wininet-url_componentsa">URL_COMPONENTS</a> structure pointed to by <i>lpUrlComponents</i> is too large. This is only the case, however, with "file://" URLs that contain space characters.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines InternetCrackUrl as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wininet/nf-wininet-ftpopenfilea">FtpOpenFile</a>



<a href="/windows/desktop/WinInet/handling-uniform-resource-locators">Handling Uniform Resource Locators</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetclosehandle">InternetCloseHandle</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetfindnextfilea">InternetFindNextFile</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetsetstatuscallback">InternetSetStatusCallback</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
