---
UID: NF:wmsdkidl.IWMPacketSize.GetMaxPacketSize
title: IWMPacketSize::GetMaxPacketSize (wmsdkidl.h)
description: The GetMaxPacketSize method retrieves the maximum size of a packet in an ASF file.
helpviewer_keywords: ["GetMaxPacketSize","GetMaxPacketSize method [windows Media Format]","GetMaxPacketSize method [windows Media Format]","IWMPacketSize interface","GetMaxPacketSize method [windows Media Format]","IWMPacketSize2 interface","IWMPacketSize interface [windows Media Format]","GetMaxPacketSize method","IWMPacketSize.GetMaxPacketSize","IWMPacketSize2 interface [windows Media Format]","GetMaxPacketSize method","IWMPacketSize2::GetMaxPacketSize","IWMPacketSize::GetMaxPacketSize","IWMPacketSizeGetMaxPacketSize","wmformat.iwmpacketsize_getmaxpacketsize","wmsdkidl/IWMPacketSize2::GetMaxPacketSize","wmsdkidl/IWMPacketSize::GetMaxPacketSize"]
old-location: wmformat\iwmpacketsize_getmaxpacketsize.htm
tech.root: wmformat
ms.assetid: 8410c524-9c27-48ac-9a48-c17cae782764
ms.date: 4/26/2023
ms.keywords: GetMaxPacketSize, GetMaxPacketSize method [windows Media Format], GetMaxPacketSize method [windows Media Format],IWMPacketSize interface, GetMaxPacketSize method [windows Media Format],IWMPacketSize2 interface, IWMPacketSize interface [windows Media Format],GetMaxPacketSize method, IWMPacketSize.GetMaxPacketSize, IWMPacketSize2 interface [windows Media Format],GetMaxPacketSize method, IWMPacketSize2::GetMaxPacketSize, IWMPacketSize::GetMaxPacketSize, IWMPacketSizeGetMaxPacketSize, wmformat.iwmpacketsize_getmaxpacketsize, wmsdkidl/IWMPacketSize2::GetMaxPacketSize, wmsdkidl/IWMPacketSize::GetMaxPacketSize
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
 - IWMPacketSize::GetMaxPacketSize
 - wmsdkidl/IWMPacketSize::GetMaxPacketSize
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
 - qasf.dll
api_name:
 - IWMPacketSize.GetMaxPacketSize
 - IWMPacketSize2.GetMaxPacketSize
---

# IWMPacketSize::GetMaxPacketSize


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetMaxPacketSize</b> method retrieves the maximum size of a <a href="/windows/desktop/wmformat/wmformat-glossary">packet</a> in an ASF file.

## -parameters

### -param pdwMaxPacketSize [out]

Pointer to a <b>DWORD</b> containing the maximum packet size, in bytes.

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
The <i>pdwMaxPacketSize</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

For more information, see the Remarks section of <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmpacketsize-setmaxpacketsize">SetMaxPacketSize</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize">IWMPacketSize Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2">IWMPacketSize2</a>