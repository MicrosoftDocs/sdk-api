---
UID: NE:wmsdkidl.WMT_ATTR_IMAGETYPE
title: WMT_ATTR_IMAGETYPE (wmsdkidl.h)
description: The WMT_ATTR_IMAGETYPE enumeration type lists image types that can be stored in the header of an ASF file.
helpviewer_keywords: ["WMT_ATTR_IMAGETYPE","WMT_ATTR_IMAGETYPE enumeration [windows Media Format]","WMT_IMAGETYPE_BITMAP","WMT_IMAGETYPE_GIF","WMT_IMAGETYPE_JPEG","wmformat.wmt_attr_imagetype","wmsdkidl/WMT_ATTR_IMAGETYPE","wmsdkidl/WMT_IMAGETYPE_BITMAP","wmsdkidl/WMT_IMAGETYPE_GIF","wmsdkidl/WMT_IMAGETYPE_JPEG"]
old-location: wmformat\wmt_attr_imagetype.htm
tech.root: wmformat
ms.assetid: 0e032796-4bbf-4307-982f-560a56506db2
ms.date: 4/26/2023
ms.keywords: WMT_ATTR_IMAGETYPE, WMT_ATTR_IMAGETYPE enumeration [windows Media Format], WMT_IMAGETYPE_BITMAP, WMT_IMAGETYPE_GIF, WMT_IMAGETYPE_JPEG, wmformat.wmt_attr_imagetype, wmsdkidl/WMT_ATTR_IMAGETYPE, wmsdkidl/WMT_IMAGETYPE_BITMAP, wmsdkidl/WMT_IMAGETYPE_GIF, wmsdkidl/WMT_IMAGETYPE_JPEG
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
req.typenames: WMT_ATTR_IMAGETYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMT_ATTR_IMAGETYPE
 - wmsdkidl/WMT_ATTR_IMAGETYPE
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
 - WMT_ATTR_IMAGETYPE
---

# WMT_ATTR_IMAGETYPE enumeration


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WMT_ATTR_IMAGETYPE</b> enumeration type lists image types that can be stored in the header of an ASF file.

## -enum-fields

### -field WMT_IMAGETYPE_BITMAP:1

The image is a device-independent bitmap.

### -field WMT_IMAGETYPE_JPEG:2

The image is in JPEG format.

### -field WMT_IMAGETYPE_GIF:3

The image is in GIF format.

## -see-also

<a href="/windows/desktop/wmformat/enumeration-types">Enumeration Types</a>
