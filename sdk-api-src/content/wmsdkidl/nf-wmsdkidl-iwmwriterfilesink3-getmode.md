---
UID: NF:wmsdkidl.IWMWriterFileSink3.GetMode
title: IWMWriterFileSink3::GetMode (wmsdkidl.h)
description: The GetMode method retrieves the supported file sink mode. More than one mode can be supported.
helpviewer_keywords: ["GetMode","GetMode method [windows Media Format]","GetMode method [windows Media Format]","IWMWriterFileSink3 interface","IWMWriterFileSink3 interface [windows Media Format]","GetMode method","IWMWriterFileSink3.GetMode","IWMWriterFileSink3::GetMode","IWMWriterFileSink3GetMode","wmformat.iwmwriterfilesink3_getmode","wmsdkidl/IWMWriterFileSink3::GetMode"]
old-location: wmformat\iwmwriterfilesink3_getmode.htm
tech.root: wmformat
ms.assetid: a8a7003e-e59f-451c-9f45-75d6d094a03b
ms.date: 4/26/2023
ms.keywords: GetMode, GetMode method [windows Media Format], GetMode method [windows Media Format],IWMWriterFileSink3 interface, IWMWriterFileSink3 interface [windows Media Format],GetMode method, IWMWriterFileSink3.GetMode, IWMWriterFileSink3::GetMode, IWMWriterFileSink3GetMode, wmformat.iwmwriterfilesink3_getmode, wmsdkidl/IWMWriterFileSink3::GetMode
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
 - IWMWriterFileSink3::GetMode
 - wmsdkidl/IWMWriterFileSink3::GetMode
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
 - IWMWriterFileSink3.GetMode
---

# IWMWriterFileSink3::GetMode


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetMode</b> method retrieves the supported file sink mode. More than one mode can be supported.

## -parameters

### -param pdwFileSinkMode [out]

Pointer to a <b>DWORD</b> containing a value from the <a href="/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_filesink_mode">WMT_FILESINK_MODE</a> enumeration type or multiple values combined with a bitwise <b>OR</b> operator.

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
<i>pdwFileSinkMode</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3">IWMWriterFileSink3 Interface</a>