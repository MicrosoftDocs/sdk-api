---
UID: NS:wmsdkidl._WMUserWebURL
title: WM_USER_WEB_URL (wmsdkidl.h)
description: The WM_USER_WEB_URL structure is used as the data item for the WM/UserWebURL complex metadata attribute.
helpviewer_keywords: ["WM_USER_WEB_URL","WM_USER_WEB_URL structure [windows Media Format]","wmformat.wm_user_web_url","wmsdkidl/WM_USER_WEB_URL"]
old-location: wmformat\wm_user_web_url.htm
tech.root: wmformat
ms.assetid: 004708cf-9bcd-469a-b770-54fa5ef1aeef
ms.date: 4/26/2023
ms.keywords: WM_USER_WEB_URL, WM_USER_WEB_URL structure [windows Media Format], wmformat.wm_user_web_url, wmsdkidl/WM_USER_WEB_URL
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
req.typenames: WM_USER_WEB_URL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WMUserWebURL
 - wmsdkidl/_WMUserWebURL
 - WM_USER_WEB_URL
 - wmsdkidl/WM_USER_WEB_URL
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
 - WM_USER_WEB_URL
---

# WM_USER_WEB_URL structure


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WM_USER_WEB_URL</b> structure is used as the data item for the <a href="/windows/desktop/wmformat/wm-userweburl">WM/UserWebURL</a> complex metadata attribute.

## -struct-fields

### -field pwszDescription

Pointer to a wide-character null-terminated string containing the description of the Web site pointed to by the URL.

### -field pwszURL

Pointer to a wide-character null-terminated string containing the URL.

## -see-also

<a href="/windows/desktop/wmformat/structures">Structures</a>