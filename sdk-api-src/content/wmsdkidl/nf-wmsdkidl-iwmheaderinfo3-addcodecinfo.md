---
UID: NF:wmsdkidl.IWMHeaderInfo3.AddCodecInfo
title: IWMHeaderInfo3::AddCodecInfo (wmsdkidl.h)
description: The AddCodecInfo method adds codec information to a file. When you copy a compressed stream from one file to another, use this method to include the information about the encoding codec in the file header.
helpviewer_keywords: ["AddCodecInfo","AddCodecInfo method [windows Media Format]","AddCodecInfo method [windows Media Format]","IWMHeaderInfo3 interface","IWMHeaderInfo3 interface [windows Media Format]","AddCodecInfo method","IWMHeaderInfo3.AddCodecInfo","IWMHeaderInfo3::AddCodecInfo","IWMHeaderInfo3AddCodecInfo","wmformat.iwmheaderinfo3_addcodecinfo","wmsdkidl/IWMHeaderInfo3::AddCodecInfo"]
old-location: wmformat\iwmheaderinfo3_addcodecinfo.htm
tech.root: wmformat
ms.assetid: 4c5bc019-e4bb-419b-91ce-779fd36d7b4c
ms.date: 4/26/2023
ms.keywords: AddCodecInfo, AddCodecInfo method [windows Media Format], AddCodecInfo method [windows Media Format],IWMHeaderInfo3 interface, IWMHeaderInfo3 interface [windows Media Format],AddCodecInfo method, IWMHeaderInfo3.AddCodecInfo, IWMHeaderInfo3::AddCodecInfo, IWMHeaderInfo3AddCodecInfo, wmformat.iwmheaderinfo3_addcodecinfo, wmsdkidl/IWMHeaderInfo3::AddCodecInfo
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
 - IWMHeaderInfo3::AddCodecInfo
 - wmsdkidl/IWMHeaderInfo3::AddCodecInfo
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
 - IWMHeaderInfo3.AddCodecInfo
---

# IWMHeaderInfo3::AddCodecInfo


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AddCodecInfo</b> method adds codec information to a file. When you copy a compressed stream from one file to another, use this method to include the information about the encoding codec in the file header.

## -parameters

### -param pwszName [in]

Pointer to a wide-character null-terminated string containing the name.

### -param pwszDescription [in]

Pointer to a wide-character null-terminated string containing the description.

### -param codecType [in]

A value from the <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_codec_info_type">WMT_CODEC_INFO_TYPE</a> enumeration specifying the codec type.

### -param cbCodecInfo [in]

The size of the codec information, in bytes.

### -param pbCodecInfo [in]

Pointer to an array of bytes that contains the codec information.

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
</table>

## -remarks

The parameters passed to this method should be obtained from the original file with a call to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo">IWMHeaderInfo2::GetCodecInfo</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3">IWMHeaderInfo3 Interface</a>