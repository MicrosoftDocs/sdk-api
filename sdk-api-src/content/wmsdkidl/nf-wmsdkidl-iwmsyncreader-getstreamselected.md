---
UID: NF:wmsdkidl.IWMSyncReader.GetStreamSelected
title: IWMSyncReader::GetStreamSelected (wmsdkidl.h)
description: The GetStreamSelected method retrieves a flag indicating whether a particular stream is currently selected.
helpviewer_keywords: ["GetStreamSelected","GetStreamSelected method [windows Media Format]","GetStreamSelected method [windows Media Format]","IWMSyncReader interface","IWMSyncReader interface [windows Media Format]","GetStreamSelected method","IWMSyncReader.GetStreamSelected","IWMSyncReader::GetStreamSelected","IWMSyncReaderGetStreamSelected","wmformat.iwmsyncreader_getstreamselected","wmsdkidl/IWMSyncReader::GetStreamSelected"]
old-location: wmformat\iwmsyncreader_getstreamselected.htm
tech.root: wmformat
ms.assetid: bcde749e-c0fd-4be8-8708-a053854a9275
ms.date: 4/26/2023
ms.keywords: GetStreamSelected, GetStreamSelected method [windows Media Format], GetStreamSelected method [windows Media Format],IWMSyncReader interface, IWMSyncReader interface [windows Media Format],GetStreamSelected method, IWMSyncReader.GetStreamSelected, IWMSyncReader::GetStreamSelected, IWMSyncReaderGetStreamSelected, wmformat.iwmsyncreader_getstreamselected, wmsdkidl/IWMSyncReader::GetStreamSelected
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
 - IWMSyncReader::GetStreamSelected
 - wmsdkidl/IWMSyncReader::GetStreamSelected
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
 - IWMSyncReader.GetStreamSelected
---

# IWMSyncReader::GetStreamSelected


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetStreamSelected</b> method retrieves a flag indicating whether a particular stream is currently selected.

## -parameters

### -param wStreamNum [in]

<b>WORD</b> containing the stream number.

### -param pSelection [out]

Pointer to a variable that receives one member of the <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_stream_selection">WMT_STREAM_SELECTION</a> enumeration type on output. This value specifies the selection status for the specified stream.

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
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
No file is open in the synchronous reader.

</td>
</tr>
</table>

## -remarks

This method is identical to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstreamselected">IWMReaderAdvanced::GetStreamSelected</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader">IWMSyncReader Interface</a>