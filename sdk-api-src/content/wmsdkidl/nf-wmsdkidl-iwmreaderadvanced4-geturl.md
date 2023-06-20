---
UID: NF:wmsdkidl.IWMReaderAdvanced4.GetURL
title: IWMReaderAdvanced4::GetURL (wmsdkidl.h)
description: The GetURL method retrieves the URL of the file being read. This URL might be different from the URL that was passed to IWMReader::Open, because the reader might have been redirected.
helpviewer_keywords: ["GetURL","GetURL method [windows Media Format]","GetURL method [windows Media Format]","IWMReaderAdvanced4 interface","IWMReaderAdvanced4 interface [windows Media Format]","GetURL method","IWMReaderAdvanced4.GetURL","IWMReaderAdvanced4::GetURL","IWMReaderAdvanced4GetURL","wmformat.iwmreaderadvanced4_geturl","wmsdkidl/IWMReaderAdvanced4::GetURL"]
old-location: wmformat\iwmreaderadvanced4_geturl.htm
tech.root: wmformat
ms.assetid: 1c17be57-da35-40f2-a216-97d6953c7311
ms.date: 4/26/2023
ms.keywords: GetURL, GetURL method [windows Media Format], GetURL method [windows Media Format],IWMReaderAdvanced4 interface, IWMReaderAdvanced4 interface [windows Media Format],GetURL method, IWMReaderAdvanced4.GetURL, IWMReaderAdvanced4::GetURL, IWMReaderAdvanced4GetURL, wmformat.iwmreaderadvanced4_geturl, wmsdkidl/IWMReaderAdvanced4::GetURL
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
 - IWMReaderAdvanced4::GetURL
 - wmsdkidl/IWMReaderAdvanced4::GetURL
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
 - IWMReaderAdvanced4.GetURL
---

# IWMReaderAdvanced4::GetURL


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetURL</b> method retrieves the URL of the file being read. This URL might be different from the URL that was passed to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-open">IWMReader::Open</a>, because the reader might have been redirected.

## -parameters

### -param pwszURL

[ out ] Pointer to a wide-character <b>null</b>-terminated string containing the URL of the file.

### -param pcchURL [in]

[ in, out ] Pointer to a variable containing the number of wide characters in <i>pwszURL</i>.

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
<b>NULL</b> pointer argument.

</td>
</tr>
</table>

## -remarks

Call this method twice. The first time, pass <b>NULL</b> as the value for <i>pwszURL</i>. The method returns the size of the string in the <i>pcchURL</i> parameter. Allocate the required amount of memory for the string and call the method again. This time, pass a pointer to the allocated buffer in the <i>pwszURL</i> parameter.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4">IWMReaderAdvanced4 Interface</a>