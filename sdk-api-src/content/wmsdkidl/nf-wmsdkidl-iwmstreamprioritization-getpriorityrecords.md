---
UID: NF:wmsdkidl.IWMStreamPrioritization.GetPriorityRecords
title: IWMStreamPrioritization::GetPriorityRecords (wmsdkidl.h)
description: The GetPriorityRecords method retrieves the list of streams and their priorities from the profile.
helpviewer_keywords: ["GetPriorityRecords","GetPriorityRecords method [windows Media Format]","GetPriorityRecords method [windows Media Format]","IWMStreamPrioritization interface","IWMStreamPrioritization interface [windows Media Format]","GetPriorityRecords method","IWMStreamPrioritization.GetPriorityRecords","IWMStreamPrioritization::GetPriorityRecords","IWMStreamPrioritizationGetPriorityRecords","wmformat.iwmstreamprioritization_getpriorityrecords","wmsdkidl/IWMStreamPrioritization::GetPriorityRecords"]
old-location: wmformat\iwmstreamprioritization_getpriorityrecords.htm
tech.root: wmformat
ms.assetid: 50b105c7-1e4f-435c-8bb6-643ea4d065bb
ms.date: 4/26/2023
ms.keywords: GetPriorityRecords, GetPriorityRecords method [windows Media Format], GetPriorityRecords method [windows Media Format],IWMStreamPrioritization interface, IWMStreamPrioritization interface [windows Media Format],GetPriorityRecords method, IWMStreamPrioritization.GetPriorityRecords, IWMStreamPrioritization::GetPriorityRecords, IWMStreamPrioritizationGetPriorityRecords, wmformat.iwmstreamprioritization_getpriorityrecords, wmsdkidl/IWMStreamPrioritization::GetPriorityRecords
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
 - IWMStreamPrioritization::GetPriorityRecords
 - wmsdkidl/IWMStreamPrioritization::GetPriorityRecords
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
 - IWMStreamPrioritization.GetPriorityRecords
---

# IWMStreamPrioritization::GetPriorityRecords


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetPriorityRecords</b> method retrieves the list of streams and their priorities from the profile.

## -parameters

### -param pRecordArray [out]

Pointer to an array of <b>WM_STREAM_PRIORITY_RECORD</b> structures. This array will receive the current stream priority data.

### -param pcRecords [in, out]

Pointer to a <b>WORD</b> that receives the count of records.

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
<i>pcRecords</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ASF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
<i>pcRecords</i> specifies fewer records than exist in the stream prioritization object.

</td>
</tr>
</table>

## -remarks

You should make two calls to <b>GetPriorityRecords</b>. On the first call, pass <b>NULL</b> as <i>pRecordArray</i>. On return, the value of <i>pcRecords</i> is set to the number of prioritization records in the stream priority object. Then you can allocate the required amount of memory for the array and pass a pointer to it as <i>pRecordArray</i> in the second call.

If you pass an array as <i>pRecordArray</i> that does not have enough elements allocated to contain the data, an error code of ASF_E_BUFFERTOOSMALL is returned. When returning this error code, the method still sets the value of <i>pcRecords</i>.

Records in a stream prioritization object are given in order of decreasing priority

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization">IWMStreamPrioritization Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamprioritization-setpriorityrecords">IWMStreamPrioritization::SetPriorityRecords</a>



<a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_priority_record">WM_STREAM_PRIORITY_RECORD</a>