---
UID: NF:wmsdkidl.IWMProfile3.AddBandwidthSharing
title: IWMProfile3::AddBandwidthSharing (wmsdkidl.h)
description: The AddBandwidthSharing method adds an existing bandwidth sharing object to the profile. Bandwidth sharing objects are created with a call to CreateNewBandwidthSharing. You must configure the bandwidth sharing object before adding it to the profile.
helpviewer_keywords: ["AddBandwidthSharing","AddBandwidthSharing method [windows Media Format]","AddBandwidthSharing method [windows Media Format]","IWMProfile3 interface","IWMProfile3 interface [windows Media Format]","AddBandwidthSharing method","IWMProfile3.AddBandwidthSharing","IWMProfile3::AddBandwidthSharing","IWMProfile3AddBandwidthSharing","wmformat.iwmprofile3_addbandwidthsharing","wmsdkidl/IWMProfile3::AddBandwidthSharing"]
old-location: wmformat\iwmprofile3_addbandwidthsharing.htm
tech.root: wmformat
ms.assetid: 174a4583-93fb-41cd-ba14-a959a28c1ea3
ms.date: 4/26/2023
ms.keywords: AddBandwidthSharing, AddBandwidthSharing method [windows Media Format], AddBandwidthSharing method [windows Media Format],IWMProfile3 interface, IWMProfile3 interface [windows Media Format],AddBandwidthSharing method, IWMProfile3.AddBandwidthSharing, IWMProfile3::AddBandwidthSharing, IWMProfile3AddBandwidthSharing, wmformat.iwmprofile3_addbandwidthsharing, wmsdkidl/IWMProfile3::AddBandwidthSharing
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
 - IWMProfile3::AddBandwidthSharing
 - wmsdkidl/IWMProfile3::AddBandwidthSharing
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
 - IWMProfile3.AddBandwidthSharing
---

# IWMProfile3::AddBandwidthSharing


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AddBandwidthSharing</b> method adds an existing bandwidth sharing object to the profile. Bandwidth sharing objects are created with a call to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing">CreateNewBandwidthSharing</a>. You must configure the bandwidth sharing object before adding it to the profile.

## -parameters

### -param pBS [in]

Pointer to the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing">IWMBandwidthSharing</a> interface of a bandwidth sharing object.

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

The bandwidth sharing object has a bandwidth sharing type value that is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unknown error occurred while adding the bandwidth sharing object to the internal collection in the profile.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_NO_STREAM</b></dt>
</dl>
</td>
<td width="60%">
The bandwidth sharing object contains no streams.

</td>
</tr>
</table>

## -remarks

Making a call to <b>AddBandwidthSharing</b> without first using the methods of <b>IWMBandwidthSharing</b> to configure the bandwidth sharing object will result in an error.

## -see-also

<a href="/windows/desktop/wmformat/bandwidth-sharing-object">Bandwidth Sharing Object</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing">IWMProfile3::GetBandwidthSharing</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-removebandwidthsharing">IWMProfile3::RemoveBandwidthSharing</a>