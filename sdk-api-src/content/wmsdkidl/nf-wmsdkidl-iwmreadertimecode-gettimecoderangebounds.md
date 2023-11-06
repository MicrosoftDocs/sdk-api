---
UID: NF:wmsdkidl.IWMReaderTimecode.GetTimecodeRangeBounds
title: IWMReaderTimecode::GetTimecodeRangeBounds (wmsdkidl.h)
description: The GetTimecodeRangeBounds method retrieves the starting and ending time codes for a specified SMPTE time code range.
helpviewer_keywords: ["GetTimecodeRangeBounds","GetTimecodeRangeBounds method [windows Media Format]","GetTimecodeRangeBounds method [windows Media Format]","IWMReaderTimecode interface","IWMReaderTimecode interface [windows Media Format]","GetTimecodeRangeBounds method","IWMReaderTimecode.GetTimecodeRangeBounds","IWMReaderTimecode::GetTimecodeRangeBounds","IWMReaderTimecodeGetTimecodeRangeBounds","wmformat.iwmreadertimecode_gettimecoderangebounds","wmsdkidl/IWMReaderTimecode::GetTimecodeRangeBounds"]
old-location: wmformat\iwmreadertimecode_gettimecoderangebounds.htm
tech.root: wmformat
ms.assetid: 5bc1f21c-0aca-4e45-ac82-898cb8b9f4cc
ms.date: 4/26/2023
ms.keywords: GetTimecodeRangeBounds, GetTimecodeRangeBounds method [windows Media Format], GetTimecodeRangeBounds method [windows Media Format],IWMReaderTimecode interface, IWMReaderTimecode interface [windows Media Format],GetTimecodeRangeBounds method, IWMReaderTimecode.GetTimecodeRangeBounds, IWMReaderTimecode::GetTimecodeRangeBounds, IWMReaderTimecodeGetTimecodeRangeBounds, wmformat.iwmreadertimecode_gettimecoderangebounds, wmsdkidl/IWMReaderTimecode::GetTimecodeRangeBounds
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
 - IWMReaderTimecode::GetTimecodeRangeBounds
 - wmsdkidl/IWMReaderTimecode::GetTimecodeRangeBounds
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
 - IWMReaderTimecode.GetTimecodeRangeBounds
---

# IWMReaderTimecode::GetTimecodeRangeBounds


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetTimecodeRangeBounds</b> method retrieves the starting and ending time codes for a specified SMPTE time code range.

## -parameters

### -param wStreamNum [in]

<b>WORD</b> containing the stream number.

### -param wRangeNum [in]

<b>WORD</b> containing the range number.

### -param pStartTimecode [out]

Pointer to a <b>DWORD</b> containing the first time code in the range.

### -param pEndTimecode [out]

Pointer to a <b>DWORD</b> containing the last time code in the range.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode">IWMReaderTimecode Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadertimecode-gettimecoderangecount">IWMReaderTimecode::GetTimecodeRangeCount</a>