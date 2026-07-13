---
UID: NF:wmsdkidl.IWMHeaderInfo3.GetAttributeCountEx
title: IWMHeaderInfo3::GetAttributeCountEx (wmsdkidl.h)
description: The GetAttributeCountEx method retrieves the total number of attributes associated with a specified stream number.
helpviewer_keywords: ["GetAttributeCountEx","GetAttributeCountEx method [windows Media Format]","GetAttributeCountEx method [windows Media Format]","IWMHeaderInfo3 interface","IWMHeaderInfo3 interface [windows Media Format]","GetAttributeCountEx method","IWMHeaderInfo3.GetAttributeCountEx","IWMHeaderInfo3::GetAttributeCountEx","IWMHeaderInfo3GetAttributeCountEx","wmformat.iwmheaderinfo3_getattributecountex","wmsdkidl/IWMHeaderInfo3::GetAttributeCountEx"]
old-location: wmformat\iwmheaderinfo3_getattributecountex.htm
tech.root: wmformat
ms.assetid: 8c56d7b6-4f59-450e-938c-b7d0bd37ea08
ms.date: 4/26/2023
ms.keywords: GetAttributeCountEx, GetAttributeCountEx method [windows Media Format], GetAttributeCountEx method [windows Media Format],IWMHeaderInfo3 interface, IWMHeaderInfo3 interface [windows Media Format],GetAttributeCountEx method, IWMHeaderInfo3.GetAttributeCountEx, IWMHeaderInfo3::GetAttributeCountEx, IWMHeaderInfo3GetAttributeCountEx, wmformat.iwmheaderinfo3_getattributecountex, wmsdkidl/IWMHeaderInfo3::GetAttributeCountEx
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
 - IWMHeaderInfo3::GetAttributeCountEx
 - wmsdkidl/IWMHeaderInfo3::GetAttributeCountEx
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
 - IWMHeaderInfo3.GetAttributeCountEx
---

# IWMHeaderInfo3::GetAttributeCountEx


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetAttributeCountEx</b> method retrieves the total number of attributes associated with a specified stream number. You can also use this method to get the number of attributes not associated with a specific stream (file-level attributes), or to get the total number of attributes in the file, regardless of stream number.

## -parameters

### -param wStreamNum [in]

<b>WORD</b> containing the stream number for which to retrieve the attribute count. Pass zero to retrieve the count of attributes that apply to the file rather than a specific stream. Pass 0xFFFF to retrieve the total count of all attributes in the file, both stream-specific and file-level.

### -param pcAttributes [out]

Pointer to a <b>WORD</b> containing the number of attributes that exist for the specified stream.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pcAttributes</i> is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
<i>wStreamNum</i> is not a valid stream number.

</td>
</tr>
</table>

## -remarks

The maximum number of attributes for a single stream is 65535, the capacity of the <b>WORD</b> parameter, <i>pcAttributes</i>. If you pass 0xFFFF as <i>wStreamNum</i>, this method will return the total number of attributes for the entire file. This number could potentially be greater than the capacity of <i>pcAttributes</i>. If the number of attributes in the file is greater than 65535, this method will produce unpredictable results. In reality, no file should ever have this many attributes. If your application makes use of an extremely large number of attributes, simply make individual calls to <b>GetAttributeCountEx</b> for each stream and for the file-level attributes.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3">IWMHeaderInfo3 Interface</a>