---
UID: NE:wmsdkidl.WM_AETYPE
title: WM_AETYPE (wmsdkidl.h)
description: The WM_AETYPE enumeration specifies the permissions for an entry in an IP address access list.
helpviewer_keywords: ["WM_AETYPE","WM_AETYPE enumeration [windows Media Format]","WM_AETYPE_EXCLUDE","WM_AETYPE_INCLUDE","wmformat.wm_aetype","wmsdkidl/WM_AETYPE","wmsdkidl/WM_AETYPE_EXCLUDE","wmsdkidl/WM_AETYPE_INCLUDE"]
old-location: wmformat\wm_aetype.htm
tech.root: wmformat
ms.assetid: 514e6745-c521-41bd-81c2-b6c24cfb0192
ms.date: 12/05/2018
ms.keywords: WM_AETYPE, WM_AETYPE enumeration [windows Media Format], WM_AETYPE_EXCLUDE, WM_AETYPE_INCLUDE, wmformat.wm_aetype, wmsdkidl/WM_AETYPE, wmsdkidl/WM_AETYPE_EXCLUDE, wmsdkidl/WM_AETYPE_INCLUDE
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
req.typenames: WM_AETYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WM_AETYPE
 - wmsdkidl/WM_AETYPE
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
 - WM_AETYPE
---

# WM_AETYPE enumeration


## -description

The <b>WM_AETYPE</b> enumeration specifies the permissions for an entry in an IP address access list.

## -enum-fields

### -field WM_AETYPE_INCLUDE:0x69

IP addresses that match the access entry are allowed to connect to the network sink.

### -field WM_AETYPE_EXCLUDE:0x65

IP addresses that match the access entry are not allowed to connect to the network sink.

## -see-also

<a href="/windows/desktop/wmformat/enumeration-types">Enumeration Types</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmaddressaccess">IWMAddressAccess Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmaddressaccess2">IWMAddressAccess2 Interface</a>
