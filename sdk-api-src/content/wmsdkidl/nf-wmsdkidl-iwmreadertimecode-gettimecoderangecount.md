---
UID: NF:wmsdkidl.IWMReaderTimecode.GetTimecodeRangeCount
title: IWMReaderTimecode::GetTimecodeRangeCount (wmsdkidl.h)
description: The GetTimecodeRangeCount method retrieves the total number of SMTPE time code ranges in a specified stream.
helpviewer_keywords: ["GetTimecodeRangeCount","GetTimecodeRangeCount method [windows Media Format]","GetTimecodeRangeCount method [windows Media Format]","IWMReaderTimecode interface","IWMReaderTimecode interface [windows Media Format]","GetTimecodeRangeCount method","IWMReaderTimecode.GetTimecodeRangeCount","IWMReaderTimecode::GetTimecodeRangeCount","IWMReaderTimecodeGetTimecodeRangeCount","wmformat.iwmreadertimecode_gettimecoderangecount","wmsdkidl/IWMReaderTimecode::GetTimecodeRangeCount"]
old-location: wmformat\iwmreadertimecode_gettimecoderangecount.htm
tech.root: wmformat
ms.assetid: df58f968-23f8-407b-b18c-569732635464
ms.date: 4/26/2023
ms.keywords: GetTimecodeRangeCount, GetTimecodeRangeCount method [windows Media Format], GetTimecodeRangeCount method [windows Media Format],IWMReaderTimecode interface, IWMReaderTimecode interface [windows Media Format],GetTimecodeRangeCount method, IWMReaderTimecode.GetTimecodeRangeCount, IWMReaderTimecode::GetTimecodeRangeCount, IWMReaderTimecodeGetTimecodeRangeCount, wmformat.iwmreadertimecode_gettimecoderangecount, wmsdkidl/IWMReaderTimecode::GetTimecodeRangeCount
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
 - IWMReaderTimecode::GetTimecodeRangeCount
 - wmsdkidl/IWMReaderTimecode::GetTimecodeRangeCount
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
 - IWMReaderTimecode.GetTimecodeRangeCount
---

# IWMReaderTimecode::GetTimecodeRangeCount


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetTimecodeRangeCount</b> method retrieves the total number of SMTPE time code ranges in a specified stream.

## -parameters

### -param wStreamNum [in]

<b>WORD</b> containing the stream number. This stream must be indexed by time code.

### -param pwRangeCount [out]

Pointer to a <b>WORD</b> containing the number of ranges. If this parameter is 0 on method return, no SMPTE ranges exist in the stream.

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



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadertimecode-gettimecoderangebounds">IWMReaderTimecode::GetTimecodeRangeBounds</a>