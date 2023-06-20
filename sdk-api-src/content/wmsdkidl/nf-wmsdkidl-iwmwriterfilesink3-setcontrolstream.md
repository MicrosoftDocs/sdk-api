---
UID: NF:wmsdkidl.IWMWriterFileSink3.SetControlStream
title: IWMWriterFileSink3::SetControlStream (wmsdkidl.h)
description: The SetControlStream method enables you to specify that a stream should be used as a control stream. You can also use this method to indicate that a previously specified control stream should no longer be used as a control stream.
helpviewer_keywords: ["IWMWriterFileSink3 interface [windows Media Format]","SetControlStream method","IWMWriterFileSink3.SetControlStream","IWMWriterFileSink3::SetControlStream","IWMWriterFileSink3SetControlStream","SetControlStream","SetControlStream method [windows Media Format]","SetControlStream method [windows Media Format]","IWMWriterFileSink3 interface","wmformat.iwmwriterfilesink3_setcontrolstream","wmsdkidl/IWMWriterFileSink3::SetControlStream"]
old-location: wmformat\iwmwriterfilesink3_setcontrolstream.htm
tech.root: wmformat
ms.assetid: c103d205-a568-4206-a66e-5473e16cfa3f
ms.date: 4/26/2023
ms.keywords: IWMWriterFileSink3 interface [windows Media Format],SetControlStream method, IWMWriterFileSink3.SetControlStream, IWMWriterFileSink3::SetControlStream, IWMWriterFileSink3SetControlStream, SetControlStream, SetControlStream method [windows Media Format], SetControlStream method [windows Media Format],IWMWriterFileSink3 interface, wmformat.iwmwriterfilesink3_setcontrolstream, wmsdkidl/IWMWriterFileSink3::SetControlStream
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
 - IWMWriterFileSink3::SetControlStream
 - wmsdkidl/IWMWriterFileSink3::SetControlStream
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
 - IWMWriterFileSink3.SetControlStream
---

# IWMWriterFileSink3::SetControlStream


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetControlStream</b> method enables you to specify that a stream should be used as a control stream. You can also use this method to indicate that a previously specified control stream should no longer be used as a control stream.

## -parameters

### -param wStreamNumber [in]

A <b>WORD</b> specifying the stream number to configure. Stream numbers must be in the range of 1 through 63.

### -param fShouldControlStartAndStop [in]

A BOOL specifying whether or not the stream should be used as a control stream.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The stream number specified by <i>wStreamNumber</i> is greater than the maximum.

</td>
</tr>
</table>

## -remarks

Control streams add accuracy to <b>Start</b> and <b>Stop</b> calls. Instead of trying to find the best starting or stopping place for the file based on times in interleaved streams, the file sink starts and stops the file at exactly the specified time in the control stream. The other streams are then synchronized with the control stream.

You can have more than one control stream, by making multiple calls to this method. The file sink will start or stop at the first encountered instance of the desired time.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3">IWMWriterFileSink3 Interface</a>