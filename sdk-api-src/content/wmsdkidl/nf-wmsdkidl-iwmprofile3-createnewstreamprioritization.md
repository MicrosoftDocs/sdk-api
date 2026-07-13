---
UID: NF:wmsdkidl.IWMProfile3.CreateNewStreamPrioritization
title: IWMProfile3::CreateNewStreamPrioritization (wmsdkidl.h)
description: The CreateNewStreamPrioritization method creates a new stream prioritization object.
helpviewer_keywords: ["CreateNewStreamPrioritization","CreateNewStreamPrioritization method [windows Media Format]","CreateNewStreamPrioritization method [windows Media Format]","IWMProfile3 interface","IWMProfile3 interface [windows Media Format]","CreateNewStreamPrioritization method","IWMProfile3.CreateNewStreamPrioritization","IWMProfile3::CreateNewStreamPrioritization","IWMProfile3CreateNewStreamPrioritization","wmformat.iwmprofile3_createnewstreamprioritization","wmsdkidl/IWMProfile3::CreateNewStreamPrioritization"]
old-location: wmformat\iwmprofile3_createnewstreamprioritization.htm
tech.root: wmformat
ms.assetid: 801a66fa-b72d-4282-953e-216fb9a56cd7
ms.date: 4/26/2023
ms.keywords: CreateNewStreamPrioritization, CreateNewStreamPrioritization method [windows Media Format], CreateNewStreamPrioritization method [windows Media Format],IWMProfile3 interface, IWMProfile3 interface [windows Media Format],CreateNewStreamPrioritization method, IWMProfile3.CreateNewStreamPrioritization, IWMProfile3::CreateNewStreamPrioritization, IWMProfile3CreateNewStreamPrioritization, wmformat.iwmprofile3_createnewstreamprioritization, wmsdkidl/IWMProfile3::CreateNewStreamPrioritization
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
 - IWMProfile3::CreateNewStreamPrioritization
 - wmsdkidl/IWMProfile3::CreateNewStreamPrioritization
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
 - IWMProfile3.CreateNewStreamPrioritization
---

# IWMProfile3::CreateNewStreamPrioritization


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>CreateNewStreamPrioritization</b> method creates a new stream prioritization object. After you create a stream prioritization object, use the methods of the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization">IWMStreamPrioritization</a> interface to configure it. The configured stream prioritization object can then be assigned to the profile with a call to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization">SetStreamPrioritization</a>.

## -parameters

### -param ppSP [out]

Pointer to receive the address of the <b>IWMStreamPrioritization</b> interface of the new object.

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
NULL was passed as <i>ppSP</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method is unable to allocate memory for the new object.

</td>
</tr>
</table>

## -remarks

A profile can only contain one stream prioritization. When you assign a new stream prioritization to a profile, the previous one will be lost.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3 Interface</a>



<a href="/windows/desktop/wmformat/stream-prioritization-object">Stream Prioritization Object</a>