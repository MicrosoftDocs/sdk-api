---
UID: NF:wmsdkidl.IWMProfile3.SetStreamPrioritization
title: IWMProfile3::SetStreamPrioritization (wmsdkidl.h)
description: The SetStreamPrioritization method assigns a stream prioritization object to the profile. A profile can contain only one stream prioritization object at a time.
helpviewer_keywords: ["IWMProfile3 interface [windows Media Format]","SetStreamPrioritization method","IWMProfile3.SetStreamPrioritization","IWMProfile3::SetStreamPrioritization","IWMProfile3SetStreamPrioritization","SetStreamPrioritization","SetStreamPrioritization method [windows Media Format]","SetStreamPrioritization method [windows Media Format]","IWMProfile3 interface","wmformat.iwmprofile3_setstreamprioritization","wmsdkidl/IWMProfile3::SetStreamPrioritization"]
old-location: wmformat\iwmprofile3_setstreamprioritization.htm
tech.root: wmformat
ms.assetid: 16dfb205-2a0b-4dc8-a8f2-8981534018f1
ms.date: 4/26/2023
ms.keywords: IWMProfile3 interface [windows Media Format],SetStreamPrioritization method, IWMProfile3.SetStreamPrioritization, IWMProfile3::SetStreamPrioritization, IWMProfile3SetStreamPrioritization, SetStreamPrioritization, SetStreamPrioritization method [windows Media Format], SetStreamPrioritization method [windows Media Format],IWMProfile3 interface, wmformat.iwmprofile3_setstreamprioritization, wmsdkidl/IWMProfile3::SetStreamPrioritization
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
 - IWMProfile3::SetStreamPrioritization
 - wmsdkidl/IWMProfile3::SetStreamPrioritization
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
 - IWMProfile3.SetStreamPrioritization
---

# IWMProfile3::SetStreamPrioritization


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetStreamPrioritization</b> method assigns a stream prioritization object to the profile. A profile can contain only one stream prioritization object at a time.

## -parameters

### -param pSP [in]

Pointer to the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization">IWMStreamPrioritization</a> interface of the stream prioritization object you want to assign to the profile.

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
<dt><b>E_INVALID_ARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pSP</i> is <b>NULL</b>.

OR

The method was unable to validate the stream prioritization object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate memory in the profile for the object.

</td>
</tr>
</table>

## -remarks

If there is already a stream prioritization object in the profile, it will be lost.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization">IWMProfile3::GetStreamPrioritization</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-removestreamprioritization">IWMProfile3::RemoveStreamPrioritization</a>