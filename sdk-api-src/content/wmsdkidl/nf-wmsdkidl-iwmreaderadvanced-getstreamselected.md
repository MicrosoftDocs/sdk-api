---
UID: NF:wmsdkidl.IWMReaderAdvanced.GetStreamSelected
title: IWMReaderAdvanced::GetStreamSelected (wmsdkidl.h)
description: The GetStreamSelected method ascertains whether a particular stream is currently selected. This method can be used only when manual stream selection has been specified.
helpviewer_keywords: ["GetStreamSelected","GetStreamSelected method [windows Media Format]","GetStreamSelected method [windows Media Format]","IWMReaderAdvanced interface","IWMReaderAdvanced interface [windows Media Format]","GetStreamSelected method","IWMReaderAdvanced.GetStreamSelected","IWMReaderAdvanced::GetStreamSelected","IWMReaderAdvancedGetStreamSelected","wmformat.iwmreaderadvanced_getstreamselected","wmsdkidl/IWMReaderAdvanced::GetStreamSelected"]
old-location: wmformat\iwmreaderadvanced_getstreamselected.htm
tech.root: wmformat
ms.assetid: 083fc743-79be-43c6-ac4b-458c74f42fa0
ms.date: 12/05/2018
ms.keywords: GetStreamSelected, GetStreamSelected method [windows Media Format], GetStreamSelected method [windows Media Format],IWMReaderAdvanced interface, IWMReaderAdvanced interface [windows Media Format],GetStreamSelected method, IWMReaderAdvanced.GetStreamSelected, IWMReaderAdvanced::GetStreamSelected, IWMReaderAdvancedGetStreamSelected, wmformat.iwmreaderadvanced_getstreamselected, wmsdkidl/IWMReaderAdvanced::GetStreamSelected
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
 - IWMReaderAdvanced::GetStreamSelected
 - wmsdkidl/IWMReaderAdvanced::GetStreamSelected
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
 - IWMReaderAdvanced.GetStreamSelected
---

# IWMReaderAdvanced::GetStreamSelected


## -description

The <b>GetStreamSelected</b> method ascertains whether a particular stream is currently selected. This method can be used only when manual stream selection has been specified.

## -parameters

### -param wStreamNum [in]

<b>WORD</b> containing the stream number. Stream numbers are in the range of 1 through 63.

### -param pSelection [out]

Pointer to one member of the <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_stream_selection">WMT_STREAM_SELECTION</a> enumeration type.

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
The <i>pSelection</i> parameter is <b>NULL</b>, or the stream number is invalid.

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
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
The reader object has not opened a file yet.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced">IWMReaderAdvanced Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setstreamsselected">IWMReaderAdvanced::SetStreamsSelected</a>



<a href="/windows/desktop/wmformat/to-use-manual-stream-selection">To Use Manual Stream Selection</a>



<a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_stream_selection">WMT_STREAM_SELECTION</a>