---
UID: NF:wmsdkidl.IWMHeaderInfo.RemoveMarker
title: IWMHeaderInfo::RemoveMarker (wmsdkidl.h)
description: The RemoveMarker method removes a marker from the header section of the ASF file.
helpviewer_keywords: ["IWMHeaderInfo interface [windows Media Format]","RemoveMarker method","IWMHeaderInfo.RemoveMarker","IWMHeaderInfo2 interface [windows Media Format]","RemoveMarker method","IWMHeaderInfo2::RemoveMarker","IWMHeaderInfo3 interface [windows Media Format]","RemoveMarker method","IWMHeaderInfo3::RemoveMarker","IWMHeaderInfo::RemoveMarker","IWMHeaderInfoRemoveMarker","RemoveMarker","RemoveMarker method [windows Media Format]","RemoveMarker method [windows Media Format]","IWMHeaderInfo interface","RemoveMarker method [windows Media Format]","IWMHeaderInfo2 interface","RemoveMarker method [windows Media Format]","IWMHeaderInfo3 interface","wmformat.iwmheaderinfo_removemarker","wmsdkidl/IWMHeaderInfo2::RemoveMarker","wmsdkidl/IWMHeaderInfo3::RemoveMarker","wmsdkidl/IWMHeaderInfo::RemoveMarker"]
old-location: wmformat\iwmheaderinfo_removemarker.htm
tech.root: wmformat
ms.assetid: b95aa113-b218-44ef-9516-20894e02ee6c
ms.date: 12/05/2018
ms.keywords: IWMHeaderInfo interface [windows Media Format],RemoveMarker method, IWMHeaderInfo.RemoveMarker, IWMHeaderInfo2 interface [windows Media Format],RemoveMarker method, IWMHeaderInfo2::RemoveMarker, IWMHeaderInfo3 interface [windows Media Format],RemoveMarker method, IWMHeaderInfo3::RemoveMarker, IWMHeaderInfo::RemoveMarker, IWMHeaderInfoRemoveMarker, RemoveMarker, RemoveMarker method [windows Media Format], RemoveMarker method [windows Media Format],IWMHeaderInfo interface, RemoveMarker method [windows Media Format],IWMHeaderInfo2 interface, RemoveMarker method [windows Media Format],IWMHeaderInfo3 interface, wmformat.iwmheaderinfo_removemarker, wmsdkidl/IWMHeaderInfo2::RemoveMarker, wmsdkidl/IWMHeaderInfo3::RemoveMarker, wmsdkidl/IWMHeaderInfo::RemoveMarker
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
 - IWMHeaderInfo::RemoveMarker
 - wmsdkidl/IWMHeaderInfo::RemoveMarker
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
 - IWMHeaderInfo.RemoveMarker
 - IWMHeaderInfo2.RemoveMarker
 - IWMHeaderInfo3.RemoveMarker
---

# IWMHeaderInfo::RemoveMarker


## -description

The <b>RemoveMarker</b> method removes a <a href="/windows/desktop/wmformat/wmformat-glossary">marker</a> from the header section of the ASF file.

## -parameters

### -param wIndex [in]

<b>WORD</b> containing the index of the marker.

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
<dt><b>ASF_E_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
There is no marker at <i>wIndex</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The object is not in a configurable state.

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

This method is not supported by the writer.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo">IWMHeaderInfo Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2">IWMHeaderInfo2</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3">IWMHeaderInfo3</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addmarker">IWMHeaderInfo::AddMarker</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker">IWMHeaderInfo::GetMarker</a>



<a href="/windows/desktop/wmformat/markers">Markers</a>