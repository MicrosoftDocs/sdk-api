---
UID: NS:wininet._INTERNET_BUFFERSW
title: INTERNET_BUFFERSW (wininet.h)
description: Contains both the data and header information. (Unicode)
helpviewer_keywords: ["*LPINTERNET_BUFFERSW","INTERNET_BUFFERS","INTERNET_BUFFERS structure [WinINet]","INTERNET_BUFFERSA","INTERNET_BUFFERSW","LPINTERNET_BUFFERS","LPINTERNET_BUFFERS structure pointer [WinINet]","_win32_internet_buffers","wininet.internet_buffers","wininet/ LPINTERNET_BUFFERS","wininet/INTERNET_BUFFERS","wininet/INTERNET_BUFFERSA","wininet/INTERNET_BUFFERSW"]
old-location: wininet\internet_buffers.htm
tech.root: wininet
ms.assetid: 9381184d-17f4-46ad-bd09-15c7e653d1b9
ms.date: 12/05/2018
ms.keywords: '*LPINTERNET_BUFFERSW, INTERNET_BUFFERS, INTERNET_BUFFERS structure [WinINet], INTERNET_BUFFERSA, INTERNET_BUFFERSW, LPINTERNET_BUFFERS, LPINTERNET_BUFFERS structure pointer [WinINet], _win32_internet_buffers, wininet.internet_buffers, wininet/ LPINTERNET_BUFFERS, wininet/INTERNET_BUFFERS, wininet/INTERNET_BUFFERSA, wininet/INTERNET_BUFFERSW'
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: INTERNET_BUFFERSW (Unicode) and INTERNET_BUFFERSA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: INTERNET_BUFFERSW, *LPINTERNET_BUFFERSW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _INTERNET_BUFFERSW
 - wininet/_INTERNET_BUFFERSW
 - LPINTERNET_BUFFERSW
 - wininet/LPINTERNET_BUFFERSW
 - INTERNET_BUFFERSW
 - wininet/INTERNET_BUFFERSW
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
 - INTERNET_BUFFERS
 - INTERNET_BUFFERSA
 - INTERNET_BUFFERSW
---

# INTERNET_BUFFERSW structure


## -description

Contains both the data and header information.

## -struct-fields

### -field dwStructSize

Size of the 
structure, in bytes.

### -field Next

Pointer to the next 
<b>INTERNET_BUFFERS</b> structure.

### -field lpcszHeader

Pointer to a string value that contains the headers. This member can be <b>NULL</b>.

### -field dwHeadersLength

Size of the headers, in <b>TCHARs</b>, if 
<b>lpcszHeader</b> is not <b>NULL</b>.

### -field dwHeadersTotal

Size of the headers, if there is not enough memory in the buffer.

### -field lpvBuffer

Pointer to the data buffer.

### -field dwBufferLength

Size of the buffer, in bytes, if 
<b>lpvBuffer</b> is not <b>NULL</b>.

### -field dwBufferTotal

Total size of the resource, in bytes.

### -field dwOffsetLow

Reserved; do not use.

### -field dwOffsetHigh

Reserved; do not use.

## -remarks

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines INTERNET_BUFFERS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wininet/nf-wininet-httpsendrequestexa">HttpSendRequestEx</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetreadfileexa">InternetReadFileEx</a>
