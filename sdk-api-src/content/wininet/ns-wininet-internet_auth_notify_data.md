---
UID: NS:wininet.INTERNET_AUTH_NOTIFY_DATA
title: INTERNET_AUTH_NOTIFY_DATA (wininet.h)
description: Contains the notification data for an authentication request.
helpviewer_keywords: ["INTERNET_AUTH_NOTIFY_DATA","INTERNET_AUTH_NOTIFY_DATA structure [WinINet]","_inet_internet_auth_notify_data_structure","wininet.internet_auth_notify_data","wininet/INTERNET_AUTH_NOTIFY_DATA"]
old-location: wininet\internet_auth_notify_data.htm
tech.root: wininet
ms.assetid: d6f36cf7-7a54-4890-aa27-ffb40997cfd6
ms.date: 12/05/2018
ms.keywords: INTERNET_AUTH_NOTIFY_DATA, INTERNET_AUTH_NOTIFY_DATA structure [WinINet], _inet_internet_auth_notify_data_structure, wininet.internet_auth_notify_data, wininet/INTERNET_AUTH_NOTIFY_DATA
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: INTERNET_AUTH_NOTIFY_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INTERNET_AUTH_NOTIFY_DATA
 - wininet/INTERNET_AUTH_NOTIFY_DATA
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
 - INTERNET_AUTH_NOTIFY_DATA
---

# INTERNET_AUTH_NOTIFY_DATA structure


## -description

Contains the notification data for an authentication request.

## -struct-fields

### -field cbStruct

Size of the structure, in bytes.

### -field dwOptions

### -field pfnNotify

Notification callback to retry 
<a href="/windows/desktop/api/wininet/nf-wininet-interneterrordlg">InternetErrorDlg</a>.

### -field dwContext

Pointer to a variable that contains an application-defined value used to identify the application context to pass to the notification function.

## -remarks

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wininet/nf-wininet-interneterrordlg">InternetErrorDlg</a>

