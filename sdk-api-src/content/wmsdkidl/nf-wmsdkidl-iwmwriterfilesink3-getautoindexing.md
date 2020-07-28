---
UID: NF:wmsdkidl.IWMWriterFileSink3.GetAutoIndexing
title: IWMWriterFileSink3::GetAutoIndexing (wmsdkidl.h)
description: The GetAutoIndexing method retrieves the current state of automatic indexing for the file.
helpviewer_keywords: ["GetAutoIndexing","GetAutoIndexing method [windows Media Format]","GetAutoIndexing method [windows Media Format]","IWMWriterFileSink3 interface","IWMWriterFileSink3 interface [windows Media Format]","GetAutoIndexing method","IWMWriterFileSink3.GetAutoIndexing","IWMWriterFileSink3::GetAutoIndexing","IWMWriterFileSink3GetAutoIndexing","wmformat.iwmwriterfilesink3_getautoindexing","wmsdkidl/IWMWriterFileSink3::GetAutoIndexing"]
old-location: wmformat\iwmwriterfilesink3_getautoindexing.htm
tech.root: wmformat
ms.assetid: a6412ce4-03ac-4777-8eb2-ef9f265a6d6c
ms.date: 12/05/2018
ms.keywords: GetAutoIndexing, GetAutoIndexing method [windows Media Format], GetAutoIndexing method [windows Media Format],IWMWriterFileSink3 interface, IWMWriterFileSink3 interface [windows Media Format],GetAutoIndexing method, IWMWriterFileSink3.GetAutoIndexing, IWMWriterFileSink3::GetAutoIndexing, IWMWriterFileSink3GetAutoIndexing, wmformat.iwmwriterfilesink3_getautoindexing, wmsdkidl/IWMWriterFileSink3::GetAutoIndexing
f1_keywords:
- wmsdkidl/IWMWriterFileSink3.GetAutoIndexing
dev_langs:
- c++
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
- IWMWriterFileSink3.GetAutoIndexing
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMWriterFileSink3::GetAutoIndexing


## -description



The <b>GetAutoIndexing</b> method retrieves the current state of automatic indexing for the file.



The writer object creates a time-based index for all new files by default. If you generate an ASF file using bit-rate mutual exclusion for audio content (multiple bit-rate audio), the resulting indexed file will not work with Windows Media Services version 4.1. If you want to stream your file using Windows Media Services 4.1, you must make sure that automatic indexing has been disabled before writing the file.


## -parameters




### -param pfAutoIndexing [out]

Pointer to a Boolean value that is True if automatic indexing is enabled for the file.


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
<i>pfAutoIndexing</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3">IWMWriterFileSink3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-setautoindexing">IWMWriterFileSink3::SetAutoIndexing</a>
 

 

