---
UID: NF:wmsdkidl.IWMProfile3.GetBandwidthSharing
title: IWMProfile3::GetBandwidthSharing (wmsdkidl.h)
description: The GetBandwidthSharing method retrieves a bandwidth sharing object from a profile.
helpviewer_keywords: ["GetBandwidthSharing","GetBandwidthSharing method [windows Media Format]","GetBandwidthSharing method [windows Media Format]","IWMProfile3 interface","IWMProfile3 interface [windows Media Format]","GetBandwidthSharing method","IWMProfile3.GetBandwidthSharing","IWMProfile3::GetBandwidthSharing","IWMProfile3GetBandwidthSharing","wmformat.iwmprofile3_getbandwidthsharing","wmsdkidl/IWMProfile3::GetBandwidthSharing"]
old-location: wmformat\iwmprofile3_getbandwidthsharing.htm
tech.root: wmformat
ms.assetid: be66ff8b-c883-4329-aaa4-e9549d0cbb9e
ms.date: 4/26/2023
ms.keywords: GetBandwidthSharing, GetBandwidthSharing method [windows Media Format], GetBandwidthSharing method [windows Media Format],IWMProfile3 interface, IWMProfile3 interface [windows Media Format],GetBandwidthSharing method, IWMProfile3.GetBandwidthSharing, IWMProfile3::GetBandwidthSharing, IWMProfile3GetBandwidthSharing, wmformat.iwmprofile3_getbandwidthsharing, wmsdkidl/IWMProfile3::GetBandwidthSharing
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
 - IWMProfile3::GetBandwidthSharing
 - wmsdkidl/IWMProfile3::GetBandwidthSharing
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
 - IWMProfile3.GetBandwidthSharing
---

# IWMProfile3::GetBandwidthSharing


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetBandwidthSharing</b> method retrieves a bandwidth sharing object from a profile.

## -parameters

### -param dwBSIndex [in]

<b>DWORD</b> containing the index number of the bandwidth sharing object you want to retrieve.

### -param ppBS [out]

Pointer to receive the address of the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing">IWMBandwidthSharing</a> interface of the object requested.

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
<i>ppBS</i> is <b>NULL</b>.

OR

<i>dwBSIndex</i> refers to an invalid index number.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method is unable to allocate memory for the bandwidth sharing object.

</td>
</tr>
</table>

## -remarks

Bandwidth sharing objects in a profile are assigned sequential index numbers in the order in which they were added to the profile. When you create multiple bandwidth sharing objects for a profile, you should keep track of the contents of each one. Otherwise you will have to examine each one to ascertain its settings.

## -see-also

<a href="/windows/desktop/wmformat/bandwidth-sharing-object">Bandwidth Sharing Object</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing">IWMProfile3::AddBandwidthSharing</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharingcount">IWMProfile3::GetBandwidthSharingCount</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-removebandwidthsharing">IWMProfile3::RemoveBandwidthSharing</a>