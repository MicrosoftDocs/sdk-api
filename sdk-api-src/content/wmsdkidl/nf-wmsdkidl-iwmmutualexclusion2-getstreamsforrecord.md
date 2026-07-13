---
UID: NF:wmsdkidl.IWMMutualExclusion2.GetStreamsForRecord
title: IWMMutualExclusion2::GetStreamsForRecord (wmsdkidl.h)
description: The GetStreamsForRecord method retrieves the list of streams that are present in a record.
helpviewer_keywords: ["GetStreamsForRecord","GetStreamsForRecord method [windows Media Format]","GetStreamsForRecord method [windows Media Format]","IWMMutualExclusion2 interface","IWMMutualExclusion2 interface [windows Media Format]","GetStreamsForRecord method","IWMMutualExclusion2.GetStreamsForRecord","IWMMutualExclusion2::GetStreamsForRecord","IWMMutualExclusion2GetStreamsForRecord","wmformat.iwmmutualexclusion2_getstreamsforrecord","wmsdkidl/IWMMutualExclusion2::GetStreamsForRecord"]
old-location: wmformat\iwmmutualexclusion2_getstreamsforrecord.htm
tech.root: wmformat
ms.assetid: a94a64e9-96c6-4aba-a5b4-f50d14c19b73
ms.date: 4/26/2023
ms.keywords: GetStreamsForRecord, GetStreamsForRecord method [windows Media Format], GetStreamsForRecord method [windows Media Format],IWMMutualExclusion2 interface, IWMMutualExclusion2 interface [windows Media Format],GetStreamsForRecord method, IWMMutualExclusion2.GetStreamsForRecord, IWMMutualExclusion2::GetStreamsForRecord, IWMMutualExclusion2GetStreamsForRecord, wmformat.iwmmutualexclusion2_getstreamsforrecord, wmsdkidl/IWMMutualExclusion2::GetStreamsForRecord
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
 - IWMMutualExclusion2::GetStreamsForRecord
 - wmsdkidl/IWMMutualExclusion2::GetStreamsForRecord
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
 - IWMMutualExclusion2.GetStreamsForRecord
---

# IWMMutualExclusion2::GetStreamsForRecord


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetStreamsForRecord</b> method retrieves the list of streams that are present in a record.

## -parameters

### -param wRecordNumber [in]

<b>WORD</b> containing the record number for which to retrieve the streams.

### -param pwStreamNumArray [out]

Pointer to an array that will receive the stream numbers. If it is <b>NULL</b>, <b>GetStreamsForRecord</b> will return the number of streams to <i>pcStreams</i>.

### -param pcStreams [in, out]

Pointer to a <b>WORD</b> containing the number of streams in the record.

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
<i>pcStreams</i> is <b>NULL</b>.

OR

<i>wRecordNumber</i> does not contain a valid record number.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ASF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The value passed as <i>pcStreams</i> is smaller than the number of streams in the record. On exit with this error code, the value at <i>pcStreams</i> will contain the correct number of streams.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method is unable to access the record for an unspecified reason.

</td>
</tr>
</table>

## -remarks

You should make two calls to <b>GetStreamsForRecord</b>. On the first call, pass <b>NULL</b> as <i>pwStreamNumArray</i>. On return, the value of <i>pcStreams</i> is set to the number of streams. Then you can allocate the amount of memory needed to hold the array and pass a pointer to it as <i>pwStreamNumArray</i> on the second call.

If you pass an array that is not large enough to contain all of the streams, an error code of ASF_E_BUFFERTOOSMALL is returned. When returning this error code, the method still sets the value at <i>pcStreams</i> to the correct number of streams.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2">IWMMutualExclusion2 Interface</a>