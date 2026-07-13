---
UID: NF:wmsdkidl.IWMReaderAdvanced.GetMaxStreamSampleSize
title: IWMReaderAdvanced::GetMaxStreamSampleSize (wmsdkidl.h)
description: The GetMaxStreamSampleSize method retrieves the maximum buffer size to be allocated for stream samples for a specified media stream.
helpviewer_keywords: ["GetMaxStreamSampleSize","GetMaxStreamSampleSize method [windows Media Format]","GetMaxStreamSampleSize method [windows Media Format]","IWMReaderAdvanced interface","IWMReaderAdvanced interface [windows Media Format]","GetMaxStreamSampleSize method","IWMReaderAdvanced.GetMaxStreamSampleSize","IWMReaderAdvanced::GetMaxStreamSampleSize","IWMReaderAdvancedGetMaxStreamSampleSize","wmformat.iwmreaderadvanced_getmaxstreamsamplesize","wmsdkidl/IWMReaderAdvanced::GetMaxStreamSampleSize"]
old-location: wmformat\iwmreaderadvanced_getmaxstreamsamplesize.htm
tech.root: wmformat
ms.assetid: 9511c269-0f88-4fdd-8d4b-c52bace14791
ms.date: 4/26/2023
ms.keywords: GetMaxStreamSampleSize, GetMaxStreamSampleSize method [windows Media Format], GetMaxStreamSampleSize method [windows Media Format],IWMReaderAdvanced interface, IWMReaderAdvanced interface [windows Media Format],GetMaxStreamSampleSize method, IWMReaderAdvanced.GetMaxStreamSampleSize, IWMReaderAdvanced::GetMaxStreamSampleSize, IWMReaderAdvancedGetMaxStreamSampleSize, wmformat.iwmreaderadvanced_getmaxstreamsamplesize, wmsdkidl/IWMReaderAdvanced::GetMaxStreamSampleSize
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
 - IWMReaderAdvanced::GetMaxStreamSampleSize
 - wmsdkidl/IWMReaderAdvanced::GetMaxStreamSampleSize
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
 - IWMReaderAdvanced.GetMaxStreamSampleSize
---

# IWMReaderAdvanced::GetMaxStreamSampleSize


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetMaxStreamSampleSize</b> method retrieves the maximum buffer size to be allocated for stream samples for a specified media stream.

## -parameters

### -param wStream [in]

Stream number.

### -param pcbMax [out]

Pointer to the maximum buffer size to be allocated.

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
<dt><b>ASF_E_INVALIDSTATE</b></dt>
</dl>
</td>
<td width="60%">
No file open for stream sample.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>wStream</i> specifies the wrong stream or <i>pcbMax</i> is a <b>NULL</b> pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced">IWMReaderAdvanced Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getallocateforstream">IWMReaderAdvanced::GetAllocateForStream</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxoutputsamplesize">IWMReaderAdvanced::GetMaxOutputSampleSize</a>