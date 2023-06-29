---
UID: NF:wmsdkidl.IWMWriterAdvanced.WriteStreamSample
title: IWMWriterAdvanced::WriteStreamSample (wmsdkidl.h)
description: The WriteStreamSample method writes a stream sample directly into an ASF file, bypassing the normal compression procedures.
helpviewer_keywords: ["IWMWriterAdvanced interface [windows Media Format]","WriteStreamSample method","IWMWriterAdvanced.WriteStreamSample","IWMWriterAdvanced::WriteStreamSample","IWMWriterAdvancedWriteStreamSample","WriteStreamSample","WriteStreamSample method [windows Media Format]","WriteStreamSample method [windows Media Format]","IWMWriterAdvanced interface","wmformat.iwmwriteradvanced_writestreamsample","wmsdkidl/IWMWriterAdvanced::WriteStreamSample"]
old-location: wmformat\iwmwriteradvanced_writestreamsample.htm
tech.root: wmformat
ms.assetid: 498bfb73-bfa5-429d-ae8a-3a691fc25fc2
ms.date: 4/26/2023
ms.keywords: IWMWriterAdvanced interface [windows Media Format],WriteStreamSample method, IWMWriterAdvanced.WriteStreamSample, IWMWriterAdvanced::WriteStreamSample, IWMWriterAdvancedWriteStreamSample, WriteStreamSample, WriteStreamSample method [windows Media Format], WriteStreamSample method [windows Media Format],IWMWriterAdvanced interface, wmformat.iwmwriteradvanced_writestreamsample, wmsdkidl/IWMWriterAdvanced::WriteStreamSample
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
 - IWMWriterAdvanced::WriteStreamSample
 - wmsdkidl/IWMWriterAdvanced::WriteStreamSample
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
 - IWMWriterAdvanced.WriteStreamSample
---

# IWMWriterAdvanced::WriteStreamSample


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WriteStreamSample</b> method writes a stream sample directly into an ASF file, bypassing the normal compression procedures. Use this method when writing a compressed stream if you already have the compressed samples. The most common use of <b>WriteStreamSample</b> is in copying streams from one file to another.

## -parameters

### -param wStreamNum [in]

<b>WORD</b> containing the stream number. Stream numbers are in the range of 1 through 63.

### -param cnsSampleTime [in]

<b>QWORD</b> containing the sample time, in 100-nanosecond units.

### -param msSampleSendTime [in]

<b>DWORD</b> containing the sample send time, in milliseconds. This parameter is not used.

### -param cnsSampleDuration [in]

<b>QWORD</b> containing the sample duration, in 100-nanosecond units. This parameter is not used.

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
<td>Indicates the sample is a key frame. Set this flag if and only if the compressed input sample is a key frame.</td>
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

Pointer to an <a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer</a> interface representing the sample.

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
<dt><b>NS_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The writer cannot currently be run.

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
</table>

## -remarks

You must manually set the WM_SF_CLEANPOINT flag for every video key frame. If you do not specify the key frames, it will not be readable. The first video sample delivered by the reading object is the first sample marked as a clean point.

When reading a stream created using stream samples, the reader and synchronous reader objects set the WM_SF_DISCONTINUITY flag for the first sample in the stream.

Normally the application provides samples to an input file on the <b>IWMWriter</b> interface, and the samples are then compressed. However, the application can use this interface to put the samples directly into the file, without compressing or otherwise modifying them.

If the output stream has a time code data unit extension and there is no time code extension on the sample, this method will fail in order not to cause problems later when the file is indexed. All other data unit extensions are optional on the sample. That means that this method will succeed if a data unit extension has been specified for the stream but no actual data extension is present in the sample. <b>WriteStreamSample</b> will write zeros into the file for samples that do not have extensions specified on the sample.

You can use both <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-writesample">IWMWriter::WriteSample</a> and <b>WriteStreamSample</b> to write uncompressed samples and compressed samples to the same stream. However, problems can arise because the writer cannot accurately gauge the bit rate and buffer window usage for the stream samples. Some samples may be dropped as a result.

## -see-also

<a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced">IWMWriterAdvanced Interface</a>



<a href="/windows/desktop/wmformat/writing-compressed-samples">Writing Compressed Samples</a>