---
UID: NF:wmsdkidl.IWMProfile3.RemoveBandwidthSharing
title: IWMProfile3::RemoveBandwidthSharing (wmsdkidl.h)
description: The RemoveBandwidthSharing method removes a bandwidth sharing object from the profile.
helpviewer_keywords: ["IWMProfile3 interface [windows Media Format]","RemoveBandwidthSharing method","IWMProfile3.RemoveBandwidthSharing","IWMProfile3::RemoveBandwidthSharing","IWMProfile3RemoveBandwidthSharing","RemoveBandwidthSharing","RemoveBandwidthSharing method [windows Media Format]","RemoveBandwidthSharing method [windows Media Format]","IWMProfile3 interface","wmformat.iwmprofile3_removebandwidthsharing","wmsdkidl/IWMProfile3::RemoveBandwidthSharing"]
old-location: wmformat\iwmprofile3_removebandwidthsharing.htm
tech.root: wmformat
ms.assetid: 3c0a90aa-154a-49c9-ab8e-0d1c4ce02641
ms.date: 4/26/2023
ms.keywords: IWMProfile3 interface [windows Media Format],RemoveBandwidthSharing method, IWMProfile3.RemoveBandwidthSharing, IWMProfile3::RemoveBandwidthSharing, IWMProfile3RemoveBandwidthSharing, RemoveBandwidthSharing, RemoveBandwidthSharing method [windows Media Format], RemoveBandwidthSharing method [windows Media Format],IWMProfile3 interface, wmformat.iwmprofile3_removebandwidthsharing, wmsdkidl/IWMProfile3::RemoveBandwidthSharing
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
 - IWMProfile3::RemoveBandwidthSharing
 - wmsdkidl/IWMProfile3::RemoveBandwidthSharing
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
 - IWMProfile3.RemoveBandwidthSharing
---

# IWMProfile3::RemoveBandwidthSharing


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>RemoveBandwidthSharing</b> method removes a bandwidth sharing object from the profile. If you do not already have a pointer to the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing">IWMBandwidthSharing</a> interface of the object you want to remove, you must obtain one with a call to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing">IWMProfile3::GetBandwidthSharing</a>.

## -parameters

### -param pBS [in]

Pointer to a bandwidth sharing object.

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
<i>pBS</i> is <b>NULL</b>.

OR

The bandwidth sharing object pointed to by <i>pBS</i> is not part of the profile.

</td>
</tr>
</table>

## -remarks

This method does not release the bandwidth sharing object from memory. You must make a call to the <b>Release</b> method.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing">IWMProfile3::AddBandwidthSharing</a>