---
UID: NS:wmsdkidl._WMClientProperties
title: WM_CLIENT_PROPERTIES (wmsdkidl.h)
description: The WM_CLIENT_PROPERTIES structure records information about the client.
helpviewer_keywords: ["WM_CLIENT_PROPERTIES","WM_CLIENT_PROPERTIES structure [windows Media Format]","wmformat.wm_client_properties","wmsdkidl/WM_CLIENT_PROPERTIES"]
old-location: wmformat\wm_client_properties.htm
tech.root: wmformat
ms.assetid: 62a5bafd-cc49-4a60-be03-038920e5b073
ms.date: 4/26/2023
ms.keywords: WM_CLIENT_PROPERTIES, WM_CLIENT_PROPERTIES structure [windows Media Format], wmformat.wm_client_properties, wmsdkidl/WM_CLIENT_PROPERTIES
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
req.typenames: WM_CLIENT_PROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WMClientProperties
 - wmsdkidl/_WMClientProperties
 - WM_CLIENT_PROPERTIES
 - wmsdkidl/WM_CLIENT_PROPERTIES
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
 - WM_CLIENT_PROPERTIES
---

# WM_CLIENT_PROPERTIES structure


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WM_CLIENT_PROPERTIES</b> structure records information about the client.

## -struct-fields

### -field dwIPAddress

<b>DWORD</b> containing the IP address.

### -field dwPort

<b>DWORD</b> containing the port number.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmclientconnections-getclientproperties">IWMClientConnections::GetClientProperties</a>



<a href="/windows/desktop/wmformat/structures">Structures</a>



<a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_net_protocol">WMT_NET_PROTOCOL</a>
