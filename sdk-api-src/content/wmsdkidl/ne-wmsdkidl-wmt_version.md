---
UID: NE:wmsdkidl.WMT_VERSION
title: WMT_VERSION (wmsdkidl.h)
description: The WMT_VERSION enumeration type defines the versions of the Windows Media Format SDK.
helpviewer_keywords: ["WMT_VERSION","WMT_VERSION enumeration [windows Media Format]","WMT_VER_4_0","WMT_VER_7_0","WMT_VER_8_0","WMT_VER_9_0","wmformat.wmt_version","wmsdkidl/WMT_VERSION","wmsdkidl/WMT_VER_4_0","wmsdkidl/WMT_VER_7_0","wmsdkidl/WMT_VER_8_0","wmsdkidl/WMT_VER_9_0"]
old-location: wmformat\wmt_version.htm
tech.root: wmformat
ms.assetid: 9ee414c6-49aa-42ad-9310-52f54b23e712
ms.date: 12/05/2018
ms.keywords: WMT_VERSION, WMT_VERSION enumeration [windows Media Format], WMT_VER_4_0, WMT_VER_7_0, WMT_VER_8_0, WMT_VER_9_0, wmformat.wmt_version, wmsdkidl/WMT_VERSION, wmsdkidl/WMT_VER_4_0, wmsdkidl/WMT_VER_7_0, wmsdkidl/WMT_VER_8_0, wmsdkidl/WMT_VER_9_0
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
req.typenames: WMT_VERSION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMT_VERSION
 - wmsdkidl/WMT_VERSION
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
 - WMT_VERSION
---

# WMT_VERSION enumeration


## -description

The <b>WMT_VERSION</b> enumeration type defines the versions of the Windows Media Format SDK. Every profile you create will have an associated version identified by one of these enumerations. The version associated with a profile dictates the types of data allowed. For example, data unit extensions were introduced with version 8. A profile defined as version 7 cannot include data unit extensions. Under most circumstances, you will create profiles for the most current version.

## -enum-fields

### -field WMT_VER_4_0:0x40000

Compatible with version 4 of the Windows Media Format SDK.

### -field WMT_VER_7_0:0x70000

Compatible with the Windows Media Format 7 SDK.

### -field WMT_VER_8_0:0x80000

Compatible with the Windows Media Format 8.2 SDK.

### -field WMT_VER_9_0:0x90000

Compatible with the Windows Media Format 9 Series SDK, and with the Windows Media Format 9.5 SDK.

## -remarks

The version assigned to a profile does not directly relate to the codecs used in the profile's individual streams. However, it is recommended that you use codecs of the same version as the profile. Unless you have specific requirements to the contrary, you should always use the latest version.

## -see-also

<a href="/windows/desktop/wmformat/enumeration-types">Enumeration Types</a>
