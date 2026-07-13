---
UID: NF:wmsdkidl.IWMProfile3.RemoveStreamPrioritization
title: IWMProfile3::RemoveStreamPrioritization (wmsdkidl.h)
description: The RemoveStreamPrioritization method removes the stream prioritization object from the profile.
helpviewer_keywords: ["IWMProfile3 interface [windows Media Format]","RemoveStreamPrioritization method","IWMProfile3.RemoveStreamPrioritization","IWMProfile3::RemoveStreamPrioritization","IWMProfile3RemoveStreamPrioritization","RemoveStreamPrioritization","RemoveStreamPrioritization method [windows Media Format]","RemoveStreamPrioritization method [windows Media Format]","IWMProfile3 interface","wmformat.iwmprofile3_removestreamprioritization","wmsdkidl/IWMProfile3::RemoveStreamPrioritization"]
old-location: wmformat\iwmprofile3_removestreamprioritization.htm
tech.root: wmformat
ms.assetid: 1522cb9f-ce3f-4183-8779-3ee112efb40b
ms.date: 4/26/2023
ms.keywords: IWMProfile3 interface [windows Media Format],RemoveStreamPrioritization method, IWMProfile3.RemoveStreamPrioritization, IWMProfile3::RemoveStreamPrioritization, IWMProfile3RemoveStreamPrioritization, RemoveStreamPrioritization, RemoveStreamPrioritization method [windows Media Format], RemoveStreamPrioritization method [windows Media Format],IWMProfile3 interface, wmformat.iwmprofile3_removestreamprioritization, wmsdkidl/IWMProfile3::RemoveStreamPrioritization
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
 - IWMProfile3::RemoveStreamPrioritization
 - wmsdkidl/IWMProfile3::RemoveStreamPrioritization
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
 - IWMProfile3.RemoveStreamPrioritization
---

# IWMProfile3::RemoveStreamPrioritization


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>RemoveStreamPrioritization</b> method removes the stream prioritization object from the profile.



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
No stream prioritization object exists in the profile.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization">IWMProfile3::GetStreamPrioritization</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization">IWMProfile3::SetStreamPrioritization</a>
