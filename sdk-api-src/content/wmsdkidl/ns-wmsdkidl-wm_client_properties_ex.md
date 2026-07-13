---
UID: NS:wmsdkidl._WMClientPropertiesEx
title: WM_CLIENT_PROPERTIES_EX (wmsdkidl.h)
description: The WM_CLIENT_PROPERTIES_EX structure holds extended client information.
helpviewer_keywords: ["WM_CLIENT_PROPERTIES_EX","WM_CLIENT_PROPERTIES_EX structure [windows Media Format]","wmformat.wm_client_properties_ex","wmsdkidl/WM_CLIENT_PROPERTIES_EX"]
old-location: wmformat\wm_client_properties_ex.htm
tech.root: wmformat
ms.assetid: 981a466d-576b-4774-bd7b-785b0ef80e72
ms.date: 4/26/2023
ms.keywords: WM_CLIENT_PROPERTIES_EX, WM_CLIENT_PROPERTIES_EX structure [windows Media Format], wmformat.wm_client_properties_ex, wmsdkidl/WM_CLIENT_PROPERTIES_EX
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
req.typenames: WM_CLIENT_PROPERTIES_EX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WMClientPropertiesEx
 - wmsdkidl/_WMClientPropertiesEx
 - WM_CLIENT_PROPERTIES_EX
 - wmsdkidl/WM_CLIENT_PROPERTIES_EX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsdkidl.h
api_name:
 - WM_CLIENT_PROPERTIES_EX
---

# WM_CLIENT_PROPERTIES_EX structure


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WM_CLIENT_PROPERTIES_EX</b> structure holds extended client information.

## -struct-fields

### -field cbSize

<b>DWORD</b> containing the size of the structure.

### -field pwszIPAddress

String containing the client's IP address in dot notation (for example, "192.168.10.2").

### -field pwszPort

String containing the client's port number.

### -field pwszDNSName

String containing the client's name on the domain name server (DNS), if known.

## -see-also

<a href="/windows/desktop/wmformat/structures">Structures</a>



<a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_client_properties">WM_CLIENT_PROPERTIES</a>
