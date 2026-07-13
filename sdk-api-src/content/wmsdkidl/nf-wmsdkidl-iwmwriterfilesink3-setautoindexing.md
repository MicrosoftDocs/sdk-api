---
UID: NF:wmsdkidl.IWMWriterFileSink3.SetAutoIndexing
title: IWMWriterFileSink3::SetAutoIndexing (wmsdkidl.h)
description: The SetAutoIndexing method enables or disables automatic indexing of the file.
helpviewer_keywords: ["IWMWriterFileSink3 interface [windows Media Format]","SetAutoIndexing method","IWMWriterFileSink3.SetAutoIndexing","IWMWriterFileSink3::SetAutoIndexing","IWMWriterFileSink3SetAutoIndexing","SetAutoIndexing","SetAutoIndexing method [windows Media Format]","SetAutoIndexing method [windows Media Format]","IWMWriterFileSink3 interface","wmformat.iwmwriterfilesink3_setautoindexing","wmsdkidl/IWMWriterFileSink3::SetAutoIndexing"]
old-location: wmformat\iwmwriterfilesink3_setautoindexing.htm
tech.root: wmformat
ms.assetid: 6c8f1c25-d752-42b6-87b7-9d6a6e38642f
ms.date: 4/26/2023
ms.keywords: IWMWriterFileSink3 interface [windows Media Format],SetAutoIndexing method, IWMWriterFileSink3.SetAutoIndexing, IWMWriterFileSink3::SetAutoIndexing, IWMWriterFileSink3SetAutoIndexing, SetAutoIndexing, SetAutoIndexing method [windows Media Format], SetAutoIndexing method [windows Media Format],IWMWriterFileSink3 interface, wmformat.iwmwriterfilesink3_setautoindexing, wmsdkidl/IWMWriterFileSink3::SetAutoIndexing
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
 - IWMWriterFileSink3::SetAutoIndexing
 - wmsdkidl/IWMWriterFileSink3::SetAutoIndexing
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
 - IWMWriterFileSink3.SetAutoIndexing
---

# IWMWriterFileSink3::SetAutoIndexing


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetAutoIndexing</b> method enables or disables automatic indexing of the file.

## -parameters

### -param fDoAutoIndexing [in]

Boolean value that is True to automatically index the file.

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
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
The header has already been received

</td>
</tr>
</table>

## -remarks

The state of automatic indexing must be set before the header is processed. After the header has been processed, any call to <b>SetAutoIndexing</b> results in an error.

Files are indexed by default. To disable indexing, you must call this method, passing False as the parameter.

If you generate an ASF file using bit-rate mutual exclusion for audio content (multiple bit-rate audio), the resulting indexed file will not work with Windows Media Services version 4.1. If you want to stream your file using Windows Media Services 4.1, you must disable automatic indexing before writing the file.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3">IWMWriterFileSink3 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-getautoindexing">IWMWriterFileSink3::GetAutoIndexing</a>



<a href="/windows/desktop/wmformat/working-with-indexes">Working with Indexes</a>