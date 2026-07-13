---
UID: NS:wmsdkidl._WMT_TIMECODE_EXTENSION_DATA
title: WMT_TIMECODE_EXTENSION_DATA (wmsdkidl.h)
description: The WMT_TIMECODE_EXTENSION_DATA structure contains information needed for a single SMPTE time code sample extension. One of these structures will be attached to every video frame that requires a SMPTE time code.
helpviewer_keywords: ["WMT_TIMECODE_EXTENSION_DATA","WMT_TIMECODE_EXTENSION_DATA structure [windows Media Format]","structure [windows Media Format]","wmformat.wmt_timecode_extension_data","wmsdkidl/WMT_TIMECODE_EXTENSION_DATA"]
old-location: wmformat\wmt_timecode_extension_data.htm
tech.root: wmformat
ms.assetid: 039c352c-d1f0-443f-acef-f730e949725c
ms.date: 4/26/2023
ms.keywords: WMT_TIMECODE_EXTENSION_DATA, WMT_TIMECODE_EXTENSION_DATA structure [windows Media Format], structure [windows Media Format], wmformat.wmt_timecode_extension_data, wmsdkidl/WMT_TIMECODE_EXTENSION_DATA
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
req.typenames: WMT_TIMECODE_EXTENSION_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WMT_TIMECODE_EXTENSION_DATA
 - wmsdkidl/_WMT_TIMECODE_EXTENSION_DATA
 - WMT_TIMECODE_EXTENSION_DATA
 - wmsdkidl/WMT_TIMECODE_EXTENSION_DATA
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
 - WMT_TIMECODE_EXTENSION_DATA
---

# WMT_TIMECODE_EXTENSION_DATA structure


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WMT_TIMECODE_EXTENSION_DATA</b> structure contains information needed for a single SMPTE time code sample extension. One of these structures will be attached to every video frame that requires a SMPTE time code.

## -struct-fields

### -field wRange

<b>WORD</b> specifying the range to which the time code belongs. See Remarks.

### -field dwTimecode

### -field dwUserbits

<b>DWORD</b> containing any information that the user desires. Typically, this member is used to store shot or take numbers, or other information pertinent to the production process.

### -field dwAmFlags

<b>DWORD</b> provided for maintaining any AM_TIMECODE flags that are present in source material. These flags are not used by any of the objects in the Windows Media Format SDK. For more information about AM_TIMECODE flags, refer to the SMPTE time code specification.


#### - Timecode

<b>DWORD</b> containing the time code. Time code is stored so that the hexadecimal value is read as if it were a decimal value. That is, the time code value 0x01133512 does not represent decimal 18035986, rather it specifies 1 hour, 13 minutes, 35 seconds, and 12 frames.

## -remarks

One of the more common SMPTE user scenarios is assembling a bunch of clips from their source reels into a prospective edit, and preserving the source reel time code in the edit. The time code in this type of file consists of a set of disjointed SMPTE ranges, where each range corresponds to the linear time code from its source reel.

Because these ranges are not guaranteed to be in any sort of time-related order (in other words, the first range may occur earlier in time than the second range), the concept of a range is supported in the Windows Media Format SDK time code index and interfaces. SMPTE time code MUST increase in time over a given range. Minor discontinuities within the range (such as dropped frames, or drop-frame counting) need not be marked within the range.

Ranges are guaranteed to be monotonically increasing (in other words, 0, 1, 2, 3, … ) with a WMV file. SMPTE time code values are guaranteed to be increasing within a given range in a WMV file, but not across ranges.

## -see-also

<a href="/windows/desktop/wmformat/structures">Structures</a>