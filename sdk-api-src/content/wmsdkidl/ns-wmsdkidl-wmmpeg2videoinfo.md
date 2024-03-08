---
UID: NS:wmsdkidl.tagWMMPEG2VIDEOINFO
title: WMMPEG2VIDEOINFO (wmsdkidl.h)
description: The WMMPEG2VIDEOINFO structure describes an MPEG-2 video stream.
helpviewer_keywords: ["WMMPEG2VIDEOINFO","WMMPEG2VIDEOINFO structure [windows Media Format]","wmformat.wmmpeg2videoinfo","wmsdkidl/WMMPEG2VIDEOINFO"]
old-location: wmformat\wmmpeg2videoinfo.htm
tech.root: wmformat
ms.assetid: e5907b04-200c-4459-971b-3680989a564f
ms.date: 4/26/2023
ms.keywords: WMMPEG2VIDEOINFO, WMMPEG2VIDEOINFO structure [windows Media Format], wmformat.wmmpeg2videoinfo, wmsdkidl/WMMPEG2VIDEOINFO
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
req.typenames: WMMPEG2VIDEOINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagWMMPEG2VIDEOINFO
 - wmsdkidl/tagWMMPEG2VIDEOINFO
 - WMMPEG2VIDEOINFO
 - wmsdkidl/WMMPEG2VIDEOINFO
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
 - WMMPEG2VIDEOINFO
---

# WMMPEG2VIDEOINFO structure


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WMMPEG2VIDEOINFO</b> structure describes an MPEG-2 video stream.

## -struct-fields

### -field hdr

<a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader2">WMVIDEOINFOHEADER2</a> structure giving header information.

### -field dwStartTimeCode

25-bit group-of-pictures (GOP) time code at start of data. This field is not used for DVD.

### -field cbSequenceHeader

Length of the sequence header, in bytes. For DVD, set this field to zero. The sequence header is given in the <b>dwSequenceHeader</b> field.

### -field dwProfile

<b>AM_MPEG2Profile</b> enumeration type that specifies the MPEG-2 profile.

### -field dwLevel

<b>AM_MPEG2Level</b> enumeration type that specifies the MPEG-2 level.

### -field dwFlags

Flag indicating preferences. Flags are defined in Dvdmedia.h.

Set undefined bits to zero or the connection will be rejected.

### -field dwSequenceHeader

Address of a buffer that contains the sequence header, including quantization matrices and the sequence extension, if required. This field is typed as a <b>DWORD</b> array to preserve the 32-bit alignment.

## -remarks

This structure is identical to the <b>MPEG2VIDEOINFO</b> structure defined in Dvdmedia.h. For more information, see the DirectShow documentation in the DirectX SDK.

## -see-also

<a href="/windows/desktop/wmformat/structures">Structures</a>