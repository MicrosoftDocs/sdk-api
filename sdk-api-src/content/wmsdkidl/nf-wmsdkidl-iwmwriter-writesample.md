---
UID: NF:wmsdkidl.IWMWriter.WriteSample
title: IWMWriter::WriteSample (wmsdkidl.h)
description: The WriteSample method passes in uncompressed data to be compressed and appended to the file that is being created.
helpviewer_keywords: ["IWMWriter interface [windows Media Format]","WriteSample method","IWMWriter.WriteSample","IWMWriter::WriteSample","IWMWriterWriteSample","WriteSample","WriteSample method [windows Media Format]","WriteSample method [windows Media Format]","IWMWriter interface","wmformat.iwmwriter_writesample","wmsdkidl/IWMWriter::WriteSample"]
old-location: wmformat\iwmwriter_writesample.htm
tech.root: wmformat
ms.assetid: ba1cf121-1d01-4e90-9ab0-95af0b6e3850
ms.date: 4/26/2023
ms.keywords: IWMWriter interface [windows Media Format],WriteSample method, IWMWriter.WriteSample, IWMWriter::WriteSample, IWMWriterWriteSample, WriteSample, WriteSample method [windows Media Format], WriteSample method [windows Media Format],IWMWriter interface, wmformat.iwmwriter_writesample, wmsdkidl/IWMWriter::WriteSample
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMWriter::WriteSample
 - wmsdkidl/IWMWriter::WriteSample
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
 - IWMWriter.WriteSample
---

# IWMWriter::WriteSample


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WriteSample</b> method passes in uncompressed data to be compressed and appended to the file that is being created.

## -parameters

### -param dwInputNum [in]

<b>DWORD</b> containing the input number.

### -param cnsSampleTime [in]

<b>QWORD</b> containing the sample time, in 100-nanosecond units.

### -param dwFlags [in]

<b>DWORD</b> containing one or more of the following flags.

<table>
<tr>
<th>Flag
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>No flag set</td>
<td>None of the conditions for the other flags applies. For example, a <a href="/windows/desktop/wmformat/wmformat-glossary">delta frame</a> in most cases would not have any flags set for it.</td>
</tr>
<tr>
<td>WM_SF_CLEANPOINT</td>
<td>Forces the sample to be written as a key frame. Setting this flag for audio inputs will have no effect, as all audio samples are cleanpoints.</td>
</tr>
<tr>
<td>WM_SF_DISCONTINUITY</td>
<td>For audio inputs, this flag helps to deal with gaps that may appear between samples. You should set this flag for the first sample after a gap.</td>
</tr>
<tr>
<td>WM_SF_DATALOSS</td>
<td>This flag is not used by the writer object.</td>
</tr>
</table>

### -param pSample [in]

Pointer to an <a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer</a> interface representing a sample.

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
The <i>dwInputNum</i> value is greater than the highest index number.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for an unspecified reason.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The writer is not running.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
The sample is not valid. This can occur when an input script stream contains a script sample that is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_NUM_PASSES</b></dt>
</dl>
</td>
<td width="60%">
The wrong number of preprocessing passes was used for the stream's output type.

Typically, this error will be returned if the stream configuration requires a preprocessing pass and a sample is passed without first configuring preprocessing. You can check for this error to determine whether a stream requires a preprocessing pass. Preprocessing passes are required only for bit-rate-based VBR.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_LATE_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The writer has received samples whose presentation times differ by an amount greater than the maximum synchronization tolerance. You can set the synchronization tolerance by calling <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance">IWMWriterAdvanced::SetSyncTolerance</a>.

This error can occur when there is more than one stream, and the application sends samples for one stream at a faster rate than the other stream. At some point, the second stream will lag too far behind the first, and the writer will return this error code.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_TOO_MUCH_DATA</b></dt>
</dl>
</td>
<td width="60%">
Samples from a real-time source are arriving faster than expected. This error is returned only if <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setlivesource">IWMWriterAdvanced::SetLiveSource</a> has been called to indicate a live source.

</td>
</tr>
</table>

## -remarks

If the output stream has a time code data unit extension and there is no time code extension on the sample, this method will fail in order not to cause problems later when the file is indexed. All other data unit extensions are optional on the sample. That means that this method will succeed if a data unit extension has been specified for the stream but no actual data extension is present in the sample. <b>WriteSample</b> will write zeros into the file for samples that do not have extensions specified on the sample.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter">IWMWriter Interface</a>



<a href="/windows/desktop/wmformat/to-write-samples">To Write Samples</a>