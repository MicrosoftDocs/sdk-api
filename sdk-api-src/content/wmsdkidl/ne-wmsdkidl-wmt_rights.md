---
UID: NE:wmsdkidl.WMT_RIGHTS
title: WMT_RIGHTS (wmsdkidl.h)
description: Defines the rights that may be specified in a DRM license.
helpviewer_keywords: ["WMT_RIGHTS","WMT_RIGHTS enumeration [windows Media Format]","WMT_RIGHT_COLLABORATIVE_PLAY","WMT_RIGHT_COPY","WMT_RIGHT_COPY_TO_CD","WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE","WMT_RIGHT_COPY_TO_SDMI_DEVICE","WMT_RIGHT_ONE_TIME","WMT_RIGHT_PLAYBACK","WMT_RIGHT_SAVE_STREAM_PROTECTED","WMT_RIGHT_SDMI_NOMORECOPIES","WMT_RIGHT_SDMI_TRIGGER","enumeration [windows Media Format]","wmformat.wmt_rights","wmsdkidl/WMT_RIGHTS","wmsdkidl/WMT_RIGHT_COLLABORATIVE_PLAY","wmsdkidl/WMT_RIGHT_COPY","wmsdkidl/WMT_RIGHT_COPY_TO_CD","wmsdkidl/WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE","wmsdkidl/WMT_RIGHT_COPY_TO_SDMI_DEVICE","wmsdkidl/WMT_RIGHT_ONE_TIME","wmsdkidl/WMT_RIGHT_PLAYBACK","wmsdkidl/WMT_RIGHT_SAVE_STREAM_PROTECTED","wmsdkidl/WMT_RIGHT_SDMI_NOMORECOPIES","wmsdkidl/WMT_RIGHT_SDMI_TRIGGER"]
old-location: wmformat\wmt_rights.htm
tech.root: wmformat
ms.assetid: 52a9a5ec-58fb-4804-8f56-4d863c738934
ms.date: 12/05/2018
ms.keywords: WMT_RIGHTS, WMT_RIGHTS enumeration [windows Media Format], WMT_RIGHT_COLLABORATIVE_PLAY, WMT_RIGHT_COPY, WMT_RIGHT_COPY_TO_CD, WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE, WMT_RIGHT_COPY_TO_SDMI_DEVICE, WMT_RIGHT_ONE_TIME, WMT_RIGHT_PLAYBACK, WMT_RIGHT_SAVE_STREAM_PROTECTED, WMT_RIGHT_SDMI_NOMORECOPIES, WMT_RIGHT_SDMI_TRIGGER, enumeration [windows Media Format], wmformat.wmt_rights, wmsdkidl/WMT_RIGHTS, wmsdkidl/WMT_RIGHT_COLLABORATIVE_PLAY, wmsdkidl/WMT_RIGHT_COPY, wmsdkidl/WMT_RIGHT_COPY_TO_CD, wmsdkidl/WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE, wmsdkidl/WMT_RIGHT_COPY_TO_SDMI_DEVICE, wmsdkidl/WMT_RIGHT_ONE_TIME, wmsdkidl/WMT_RIGHT_PLAYBACK, wmsdkidl/WMT_RIGHT_SAVE_STREAM_PROTECTED, wmsdkidl/WMT_RIGHT_SDMI_NOMORECOPIES, wmsdkidl/WMT_RIGHT_SDMI_TRIGGER
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
req.typenames: WMT_RIGHTS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMT_RIGHTS
 - wmsdkidl/WMT_RIGHTS
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
 - WMT_RIGHTS
---

# WMT_RIGHTS enumeration


## -description

The <b>WMT_RIGHTS</b> enumeration type defines the rights that may be specified in a DRM license.

## -enum-fields

### -field WMT_RIGHT_PLAYBACK:0x1

Specifies the right to play content without restriction.

### -field WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE:0x2

Specifies the right to copy content to a device not compliant with the <a href="/windows/desktop/wmformat/wmformat-glossary">Secure Digital Music Initiative (SDMI)</a>.

### -field WMT_RIGHT_COPY_TO_CD:0x8

Specifies the right to copy content to a CD.

### -field WMT_RIGHT_COPY_TO_SDMI_DEVICE:0x10

Specifies the right to copy content to a device compliant with the Secure Digital Music Initiative (SDMI).

### -field WMT_RIGHT_ONE_TIME:0x20

Specifies the right to play content one time only.

### -field WMT_RIGHT_SAVE_STREAM_PROTECTED:0x40

Specifies the right to save content from a server.

### -field WMT_RIGHT_COPY:0x80

Specifies the right to copy content. Windows Media DRM 10 regulates the devices to which the content can be copied by using output protection levels (OPLs).

### -field WMT_RIGHT_COLLABORATIVE_PLAY:0x100

Specifies the right to play content as part of an online scenario where multiple participants can contribute songs from their collection to a shared playlist.

### -field WMT_RIGHT_SDMI_TRIGGER:0x10000

Reserved for future use. Do not use.

### -field WMT_RIGHT_SDMI_NOMORECOPIES:0x20000

Reserved for future use. Do not use.

## -remarks

These values are bit flags, so one or more can be set by combining them with the bitwise <b>OR</b> operator.

When using Windows Media DRM 10, <b>WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE</b>, <b>WMT_RIGHT_COPY_TO_SDMI_DEVICE</b>, and <b>WMT_RIGHT_COPY_TO_CD</b> are superseded by <b>WMT_RIGHT_COPY</b>. Limitations on the devices to which the content may be copied are specified by using output protection levels (OPLs).

## -see-also

<a href="/windows/desktop/wmformat/enumeration-types">Enumeration Types</a>



<a href="/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)">WAVEFORMATEX</a>
