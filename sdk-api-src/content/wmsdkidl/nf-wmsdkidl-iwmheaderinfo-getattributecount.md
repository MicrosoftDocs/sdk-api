---
UID: NF:wmsdkidl.IWMHeaderInfo.GetAttributeCount
title: IWMHeaderInfo::GetAttributeCount (wmsdkidl.h)
description: The GetAttributeCount method returns the number of attributes defined in the header section of the ASF file. This method is replaced by IWMHeaderInfo3::GetAttributeCountEx and IWMHeaderInfo3::GetAttributeIndices, and should no longer be used.
helpviewer_keywords: ["GetAttributeCount","GetAttributeCount method [windows Media Format]","GetAttributeCount method [windows Media Format]","IWMHeaderInfo interface","GetAttributeCount method [windows Media Format]","IWMHeaderInfo2 interface","GetAttributeCount method [windows Media Format]","IWMHeaderInfo3 interface","IWMHeaderInfo interface [windows Media Format]","GetAttributeCount method","IWMHeaderInfo.GetAttributeCount","IWMHeaderInfo2 interface [windows Media Format]","GetAttributeCount method","IWMHeaderInfo2::GetAttributeCount","IWMHeaderInfo3 interface [windows Media Format]","GetAttributeCount method","IWMHeaderInfo3::GetAttributeCount","IWMHeaderInfo::GetAttributeCount","IWMHeaderInfoGetAttributeCount","wmformat.iwmheaderinfo_getattributecount","wmsdkidl/IWMHeaderInfo2::GetAttributeCount","wmsdkidl/IWMHeaderInfo3::GetAttributeCount","wmsdkidl/IWMHeaderInfo::GetAttributeCount"]
old-location: wmformat\iwmheaderinfo_getattributecount.htm
tech.root: wmformat
ms.assetid: d5f0be62-4f15-45ca-8593-f5703a1f932a
ms.date: 4/26/2023
ms.keywords: GetAttributeCount, GetAttributeCount method [windows Media Format], GetAttributeCount method [windows Media Format],IWMHeaderInfo interface, GetAttributeCount method [windows Media Format],IWMHeaderInfo2 interface, GetAttributeCount method [windows Media Format],IWMHeaderInfo3 interface, IWMHeaderInfo interface [windows Media Format],GetAttributeCount method, IWMHeaderInfo.GetAttributeCount, IWMHeaderInfo2 interface [windows Media Format],GetAttributeCount method, IWMHeaderInfo2::GetAttributeCount, IWMHeaderInfo3 interface [windows Media Format],GetAttributeCount method, IWMHeaderInfo3::GetAttributeCount, IWMHeaderInfo::GetAttributeCount, IWMHeaderInfoGetAttributeCount, wmformat.iwmheaderinfo_getattributecount, wmsdkidl/IWMHeaderInfo2::GetAttributeCount, wmsdkidl/IWMHeaderInfo3::GetAttributeCount, wmsdkidl/IWMHeaderInfo::GetAttributeCount
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
 - IWMHeaderInfo::GetAttributeCount
 - wmsdkidl/IWMHeaderInfo::GetAttributeCount
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
 - IWMHeaderInfo.GetAttributeCount
 - IWMHeaderInfo2.GetAttributeCount
 - IWMHeaderInfo3.GetAttributeCount
---

# IWMHeaderInfo::GetAttributeCount


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetAttributeCount</b> method returns the number of attributes defined in the header section of the ASF file. This method is replaced by <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributecountex">IWMHeaderInfo3::GetAttributeCountEx</a> and <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices">IWMHeaderInfo3::GetAttributeIndices</a>, and should no longer be used.

## -parameters

### -param wStreamNum [in]

<b>WORD</b> containing the stream number. Pass zero for file-level attributes.

### -param pcAttributes [out]

Pointer to a count of the attributes.

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
The object is not in a configurable state, or no profile has been set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>wStreamNum</i> is not a valid stream number, or <i>pcAttributes</i> is <b>NULL</b>.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for an unspecified reason.

</td>
</tr>
</table>

## -remarks

Attributes in MP3 files cannot be specific to a particular stream. For MP3 files, always set the stream number to zero.

## -see-also

<a href="/windows/desktop/wmformat/attributes">Attributes</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo">IWMHeaderInfo Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2">IWMHeaderInfo2</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3">IWMHeaderInfo3</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute">IWMHeaderInfo::SetAttribute</a>