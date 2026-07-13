---
UID: NF:wininet.GopherGetAttributeA
title: GopherGetAttributeA function (wininet.h)
description: Retrieves the specific attribute information from the server. (ANSI)
helpviewer_keywords: ["GopherGetAttributeA", "wininet/GopherGetAttributeA"]
old-location: wininet\gophergetattribute.htm
tech.root: wininet
ms.assetid: c9e95532-8c65-45fb-acd0-a1f09cee2ce2
ms.date: 12/05/2018
ms.keywords: GopherGetAttribute, GopherGetAttribute function [WinINet], GopherGetAttributeA, GopherGetAttributeW, _inet_gophergetattribute_function, wininet.gophergetattribute, wininet/GopherGetAttribute, wininet/GopherGetAttributeA, wininet/GopherGetAttributeW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GopherGetAttributeW (Unicode) and GopherGetAttributeA (ANSI)
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
 - GopherGetAttributeA
 - wininet/GopherGetAttributeA
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
 - GopherGetAttribute
 - GopherGetAttributeA
 - GopherGetAttributeW
---

# GopherGetAttributeA function


## -description

<p class="CCE_Message">[The <b>GopherGetAttribute</b> function is available for use in the operating systems specified in the Requirements section.]

Retrieves the specific attribute information from the server.

## -parameters

### -param hConnect [in]

Handle to a Gopher session returned by 
<a href="/windows/desktop/api/wininet/nf-wininet-internetconnecta">InternetConnect</a>.

### -param lpszLocator [in]

Pointer to a <b>null</b>-terminated string that identifies the item at the Gopher server on which to return attribute information.

### -param lpszAttributeName [in]

Pointer to a space-delimited string specifying the names of attributes to return. If 
<i>lpszAttributeName</i> is <b>NULL</b>, 
<b>GopherGetAttribute</b> returns information about all attributes.

### -param lpBuffer [out]

Pointer to an application-defined buffer from which attribute information is retrieved.

### -param dwBufferLength [in]

Size of the 
<i>lpBuffer</i> buffer, in <b>TCHARs</b>.

### -param lpdwCharactersReturned [out]

Pointer to a variable that contains the number of characters read into the 
<i>lpBuffer</i> buffer.

### -param lpfnEnumerator [in]

Pointer to a <a href="/windows/desktop/api/wininet/nc-wininet-gopher_attribute_enumerator">GopherAttributeEnumerator</a> callback function that enumerates each attribute of the locator. This parameter is optional. If it is <b>NULL</b>, all  Gopher attribute information is placed into 
<i>lpBuffer</i>. If 
<i>lpfnEnumerator</i> is specified, the callback function is called once for each attribute of the object.
				


The callback function receives the address of a single 
<a href="/windows/desktop/api/wininet/ns-wininet-gopher_attribute_type">GOPHER_ATTRIBUTE_TYPE</a> structure with each call. The enumeration callback function allows the application to avoid having to parse the Gopher attribute information.

### -param dwContext [in]

Application-defined value that associates this operation with any application data.

## -returns

Returns <b>TRUE</b> if the request is satisfied, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> or 
<a href="/windows/desktop/api/wininet/nf-wininet-internetgetlastresponseinfoa">InternetGetLastResponseInfo</a>.

## -remarks

Generally, applications call this function after calling 
<a href="/windows/desktop/api/wininet/nf-wininet-gopherfindfirstfilea">GopherFindFirstFile</a> or 
<a href="/windows/desktop/api/wininet/nf-wininet-internetfindnextfilea">InternetFindNextFile</a>.

The size of the 
<i>lpBuffer</i> parameter must be equal to or greater than the value of <b>MIN_GOPHER_ATTRIBUTE_LENGTH</b>.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines GopherGetAttribute as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
