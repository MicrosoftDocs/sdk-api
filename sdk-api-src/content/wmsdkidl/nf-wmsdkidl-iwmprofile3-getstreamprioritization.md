---
UID: NF:wmsdkidl.IWMProfile3.GetStreamPrioritization
title: IWMProfile3::GetStreamPrioritization (wmsdkidl.h)
description: The GetStreamPrioritization method retrieves the stream prioritization that exists in the profile.
helpviewer_keywords: ["GetStreamPrioritization","GetStreamPrioritization method [windows Media Format]","GetStreamPrioritization method [windows Media Format]","IWMProfile3 interface","IWMProfile3 interface [windows Media Format]","GetStreamPrioritization method","IWMProfile3.GetStreamPrioritization","IWMProfile3::GetStreamPrioritization","IWMProfile3GetStreamPrioritization","wmformat.iwmprofile3_getstreamprioritization","wmsdkidl/IWMProfile3::GetStreamPrioritization"]
old-location: wmformat\iwmprofile3_getstreamprioritization.htm
tech.root: wmformat
ms.assetid: 09545c1e-8090-4526-9faf-6cb2cb369208
ms.date: 4/26/2023
ms.keywords: GetStreamPrioritization, GetStreamPrioritization method [windows Media Format], GetStreamPrioritization method [windows Media Format],IWMProfile3 interface, IWMProfile3 interface [windows Media Format],GetStreamPrioritization method, IWMProfile3.GetStreamPrioritization, IWMProfile3::GetStreamPrioritization, IWMProfile3GetStreamPrioritization, wmformat.iwmprofile3_getstreamprioritization, wmsdkidl/IWMProfile3::GetStreamPrioritization
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
 - IWMProfile3::GetStreamPrioritization
 - wmsdkidl/IWMProfile3::GetStreamPrioritization
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
 - IWMProfile3.GetStreamPrioritization
---

# IWMProfile3::GetStreamPrioritization


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetStreamPrioritization</b> method retrieves the stream prioritization that exists in the profile.

## -parameters

### -param ppSP [out]

Pointer to receive the address of the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization">IWMStreamPrioritization</a> interface of the stream prioritization object in the profile.

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
<i>ppSP</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method is unable to allocate memory for the stream prioritization object

</td>
</tr>
</table>

## -remarks

Many profiles do not have a stream prioritization assigned to them. If you call <b>GetStreamPrioritization</b> on such a profile, no error is returned, but the retrieved address is <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-removestreamprioritization">IWMProfile3::RemoveStreamPrioritization</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization">IWMProfile3::SetStreamPrioritization</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization">IWMStreamPrioritization Interface</a>



<a href="/windows/desktop/wmformat/stream-prioritization-object">Stream Prioritization Object</a>