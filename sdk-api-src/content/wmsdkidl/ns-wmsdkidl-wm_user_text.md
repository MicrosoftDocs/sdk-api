---
UID: NS:wmsdkidl._WMUserText
title: WM_USER_TEXT (wmsdkidl.h)
description: The WM_USER_TEXT structure is used as the data item for the WM/Text complex metadata attribute.
helpviewer_keywords: ["WM_USER_TEXT","WM_USER_TEXT structure [windows Media Format]","wmformat.wm_user_text","wmsdkidl/WM_USER_TEXT"]
old-location: wmformat\wm_user_text.htm
tech.root: wmformat
ms.assetid: 49a8faf1-2af4-4c47-bbac-d8745c0f60a1
ms.date: 12/05/2018
ms.keywords: WM_USER_TEXT, WM_USER_TEXT structure [windows Media Format], wmformat.wm_user_text, wmsdkidl/WM_USER_TEXT
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
req.typenames: WM_USER_TEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WMUserText
 - wmsdkidl/_WMUserText
 - WM_USER_TEXT
 - wmsdkidl/WM_USER_TEXT
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
 - WM_USER_TEXT
---

# WM_USER_TEXT structure


## -description

The <b>WM_USER_TEXT</b> structure is used as the data item for the <a href="/windows/desktop/wmformat/wm-text">WM/Text</a> complex metadata attribute.

## -struct-fields

### -field pwszDescription

Pointer to a wide-character null-terminated string containing the description of the text entry.

### -field pwszText

Pointer to a wide-character null-terminated string containing the text.

## -see-also

<a href="/windows/desktop/wmformat/structures">Structures</a>