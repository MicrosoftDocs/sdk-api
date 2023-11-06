---
UID: NF:wmsdkidl.IWMSyncReader.GetMaxOutputSampleSize
title: IWMSyncReader::GetMaxOutputSampleSize (wmsdkidl.h)
description: The GetMaxOutputSampleSize method retrieves the maximum sample size for a specified output of the file open in the synchronous reader.
helpviewer_keywords: ["GetMaxOutputSampleSize","GetMaxOutputSampleSize method [windows Media Format]","GetMaxOutputSampleSize method [windows Media Format]","IWMSyncReader interface","IWMSyncReader interface [windows Media Format]","GetMaxOutputSampleSize method","IWMSyncReader.GetMaxOutputSampleSize","IWMSyncReader::GetMaxOutputSampleSize","IWMSyncReaderGetMaxOutputSampleSize","wmformat.iwmsyncreader_getmaxoutputsamplesize","wmsdkidl/IWMSyncReader::GetMaxOutputSampleSize"]
old-location: wmformat\iwmsyncreader_getmaxoutputsamplesize.htm
tech.root: wmformat
ms.assetid: 84fbc2c7-001b-4339-a7df-89914274a72b
ms.date: 4/26/2023
ms.keywords: GetMaxOutputSampleSize, GetMaxOutputSampleSize method [windows Media Format], GetMaxOutputSampleSize method [windows Media Format],IWMSyncReader interface, IWMSyncReader interface [windows Media Format],GetMaxOutputSampleSize method, IWMSyncReader.GetMaxOutputSampleSize, IWMSyncReader::GetMaxOutputSampleSize, IWMSyncReaderGetMaxOutputSampleSize, wmformat.iwmsyncreader_getmaxoutputsamplesize, wmsdkidl/IWMSyncReader::GetMaxOutputSampleSize
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
 - IWMSyncReader::GetMaxOutputSampleSize
 - wmsdkidl/IWMSyncReader::GetMaxOutputSampleSize
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
 - IWMSyncReader.GetMaxOutputSampleSize
---

# IWMSyncReader::GetMaxOutputSampleSize


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetMaxOutputSampleSize</b> method retrieves the maximum sample size for a specified output of the file open in the synchronous reader.

## -parameters

### -param dwOutput [in]

<b>DWORD</b> containing the output number for which you want to retrieve the maximum sample size.

### -param pcbMax [out]

Pointer to a <b>DWORD</b> value that receives the maximum sample size, in bytes, for the output specified in <i>dwOutput</i>.

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
<i>pcbMax</i> is <b>NULL</b>.

OR

<i>dwOutput</i> specifies an invalid output number.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ASF_E_INVALIDSTATE</b></dt>
</dl>
</td>
<td width="60%">
No file is opened in the synchronous reader.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_NOT_CONFIGURED</b></dt>
</dl>
</td>
<td width="60%">
The specified output is not currently configured for playback.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The synchronous reader failed to initialize an internal object.

</td>
</tr>
</table>

## -remarks

In some scenarios, such as multiple bit rate streaming, the output encompasses several streams. The size returned is the maximum sample size for all of the streams associated with the specified output.

You can retrieve the maximum sample size for a specific stream by using <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxstreamsamplesize">IWMSyncReader::GetMaxStreamSampleSize</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader">IWMSyncReader Interface</a>