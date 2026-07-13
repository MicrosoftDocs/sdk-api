---
UID: NF:wmsdkidl.IWMSyncReader2.SetRangeByTimecode
title: IWMSyncReader2::SetRangeByTimecode (wmsdkidl.h)
description: The SetRangeByTimecode method sets a starting and ending time, based on SMPTE time codes, for playback of a file.
helpviewer_keywords: ["IWMSyncReader2 interface [windows Media Format]","SetRangeByTimecode method","IWMSyncReader2.SetRangeByTimecode","IWMSyncReader2::SetRangeByTimecode","IWMSyncReader2SetRangeByTimecode","SetRangeByTimecode","SetRangeByTimecode method [windows Media Format]","SetRangeByTimecode method [windows Media Format]","IWMSyncReader2 interface","wmformat.iwmsyncreader2_setrangebytimecode","wmsdkidl/IWMSyncReader2::SetRangeByTimecode"]
old-location: wmformat\iwmsyncreader2_setrangebytimecode.htm
tech.root: wmformat
ms.assetid: 304564b1-6ae3-4e1c-bea9-7a49c522a914
ms.date: 4/26/2023
ms.keywords: IWMSyncReader2 interface [windows Media Format],SetRangeByTimecode method, IWMSyncReader2.SetRangeByTimecode, IWMSyncReader2::SetRangeByTimecode, IWMSyncReader2SetRangeByTimecode, SetRangeByTimecode, SetRangeByTimecode method [windows Media Format], SetRangeByTimecode method [windows Media Format],IWMSyncReader2 interface, wmformat.iwmsyncreader2_setrangebytimecode, wmsdkidl/IWMSyncReader2::SetRangeByTimecode
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMSyncReader2::SetRangeByTimecode
 - wmsdkidl/IWMSyncReader2::SetRangeByTimecode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMSyncReader2.SetRangeByTimecode
---

# IWMSyncReader2::SetRangeByTimecode


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetRangeByTimecode</b> method sets a starting and ending time, based on SMPTE time codes, for playback of a file.

## -parameters

### -param wStreamNum [in]

<b>WORD</b> containing the stream number.

### -param pStart [in]

Pointer to a <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data">WMT_TIMECODE_EXTENSION_DATA</a> structure containing the starting time code.

### -param pEnd [in]

Pointer to a <b>WMT_TIMECODE_EXTENSION_DATA</b> structure containing the ending time code.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

For the method to succeed, the file must be indexed by SMPTE time code.

If the call is successful, all streams are synchronized to the same position based on presentation time.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader2">IWMSyncReader2 Interface</a>