---
UID: NF:wmsdkidl.IWMSyncReader.GetNextSample
title: IWMSyncReader::GetNextSample (wmsdkidl.h)
description: The GetNextSample method retrieves the next sample from the file.
helpviewer_keywords: ["GetNextSample","GetNextSample method [windows Media Format]","GetNextSample method [windows Media Format]","IWMSyncReader interface","IWMSyncReader interface [windows Media Format]","GetNextSample method","IWMSyncReader.GetNextSample","IWMSyncReader::GetNextSample","IWMSyncReaderGetNextSample","wmformat.iwmsyncreader_getnextsample","wmsdkidl/IWMSyncReader::GetNextSample"]
old-location: wmformat\iwmsyncreader_getnextsample.htm
tech.root: wmformat
ms.assetid: 948047b3-3b87-4381-9320-c9602716ade2
ms.date: 4/26/2023
ms.keywords: GetNextSample, GetNextSample method [windows Media Format], GetNextSample method [windows Media Format],IWMSyncReader interface, IWMSyncReader interface [windows Media Format],GetNextSample method, IWMSyncReader.GetNextSample, IWMSyncReader::GetNextSample, IWMSyncReaderGetNextSample, wmformat.iwmsyncreader_getnextsample, wmsdkidl/IWMSyncReader::GetNextSample
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
 - IWMSyncReader::GetNextSample
 - wmsdkidl/IWMSyncReader::GetNextSample
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
 - IWMSyncReader.GetNextSample
---

# IWMSyncReader::GetNextSample


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetNextSample</b> method retrieves the next sample from the file.

## -parameters

### -param wStreamNum [in]

<b>WORD</b> containing the stream number for which you would like a sample. If you pass zero, the next sample in the file is returned, regardless of stream number.

### -param ppSample [out]

Pointer to a buffer that receives the sample. Set to <b>NULL</b> to retrieve the sample time without getting the sample. If set to <b>NULL</b>, <i>pcnsDuration</i> and <i>pdwFlags</i> must both be set to <b>NULL</b> as well.

### -param pcnsSampleTime [out]

Pointer to a <b>QWORD</b> variable that receives the sample time in 100-nanosecond units.

### -param pcnsDuration [out]

Pointer to <b>QWORD</b> variable that receives the duration of the sample in 100-nanosecond units.

### -param pdwFlags [out]

Pointer to a <b>DWORD</b> containing one or more of the following flags.

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
<td>Indicates that the sample does not require any other samples to be decompressed. All audio samples and all video samples that are key frames are cleanpoints.</td>
</tr>
<tr>
<td>WM_SF_DISCONTINUITY</td>
<td>The data stream has a gap in it, which could be due to a seek, a network loss, or other reason. This can be useful extra information for an application such as a codec or renderer. The flag is set on the first piece of data following the gap.</td>
</tr>
<tr>
<td>WM_SF_DATALOSS</td>
<td>Some data has been lost between the previous sample and the sample with this flag set.</td>
</tr>
</table>

### -param pdwOutputNum [out]

Pointer to a <b>DWORD</b> that receives the output number.

### -param pwStreamNum [out]

Pointer to a <b>WORD</b> that receives the stream number.

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
<dt><b>NS_E_NO_MORE_SAMPLES</b></dt>
</dl>
</td>
<td width="60%">
All the samples in the file have been read.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
A problem occurred with a call within the method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>wStreamNum</i> specifies a stream number that is not valid.

OR

<i>pcnsSampleTime</i> is <b>NULL</b>

OR

<i>ppSample</i>, <i>pcnsDuration</i>, or <i>pdwFlags</i> is <b>NULL</b>, but one or both of the others are not.

OR

<i>wStreamNum</i> is 0 and both <i>pdwOutputNum</i> and <i>pwStreamNum</i> are <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
No file is open and ready for reading by the synchronous reader.

OR

<i>wStreamNum</i> specifies a stream number that is turned off (not selected for reading).

</td>
</tr>
</table>

## -remarks

Both compressed and uncompressed samples are delivered by this method, depending upon whether you have called <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples">SetReadStreamSamples</a> for the streams in the file. This is the only method to retrieve samples using the synchronous reader.

To begin receiving samples from anywhere in the file other than the beginning, you must first specify a range for playback. To specify a playback range based on presentation times, use the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrange">SetRange</a> method. To set a range using frame numbers, use the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe">SetRangeByFrame</a> method. When you have received all of the samples in the file, or in the range if you specified one, the next call made to <b>GetNextSample</b> returns NS_E_NO_MORE_SAMPLES.

The timeline is presentation time if no output setting is specified. To get early delivery for a stream, use <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting">SetOutputSetting</a>.

You can call <b>GetNextSample</b> in one of three ways:

<ul>
<li>If you pass a non-zero value as <i>wStreamNum</i>, you will get the next sample for the specified stream number. In this case, you can pass <b>NULL</b> for both <i>pdwOutputNum</i> and <i>pwStreamNum</i>.</li>
<li>If you pass zero as <i>wStreamNum</i>, and are using output numbers, you can pass <b>NULL</b> for <i>pwStreamNum</i>. In this case you must pass a valid address for <i>pdwOutputNum</i>.</li>
<li>If you pass zero as <i>wStreamNum</i>, and are not using output numbers, you can pass <b>NULL</b> for <i>pdwOutputNum</i>. In this case you must pass a valid address for <i>pwStreamNum</i>.</li>
</ul>
You can also use <i>GetNextSample</i> to retrieve precise times for video frames when reading compressed data. For more information, see To Retrieve Accurate Presentation Times for Compressed Samples by Frame.

<div class="alert"><b>Note</b>  To ensure that you get correct sample durations from this method, you must configure the output for the stream. Call the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting">SetOutputSetting</a> method to set the g_wszVideoSampleDurations setting to <b>TRUE</b>. Subsequent calls to <b>GetNextSample</b> will return correct sample durations.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader">IWMSyncReader Interface</a>
