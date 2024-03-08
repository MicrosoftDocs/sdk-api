---
UID: NF:wmsdkidl.IWMProfile3.CreateNewBandwidthSharing
title: IWMProfile3::CreateNewBandwidthSharing (wmsdkidl.h)
description: The CreateNewBandwidthSharing method creates a new bandwidth sharing object.
helpviewer_keywords: ["CreateNewBandwidthSharing","CreateNewBandwidthSharing method [windows Media Format]","CreateNewBandwidthSharing method [windows Media Format]","IWMProfile3 interface","IWMProfile3 interface [windows Media Format]","CreateNewBandwidthSharing method","IWMProfile3.CreateNewBandwidthSharing","IWMProfile3::CreateNewBandwidthSharing","IWMProfile3CreateNewBandwidthSharing","wmformat.iwmprofile3_createnewbandwidthsharing","wmsdkidl/IWMProfile3::CreateNewBandwidthSharing"]
old-location: wmformat\iwmprofile3_createnewbandwidthsharing.htm
tech.root: wmformat
ms.assetid: ab6c9903-95ea-499b-be75-ff57328336f0
ms.date: 4/26/2023
ms.keywords: CreateNewBandwidthSharing, CreateNewBandwidthSharing method [windows Media Format], CreateNewBandwidthSharing method [windows Media Format],IWMProfile3 interface, IWMProfile3 interface [windows Media Format],CreateNewBandwidthSharing method, IWMProfile3.CreateNewBandwidthSharing, IWMProfile3::CreateNewBandwidthSharing, IWMProfile3CreateNewBandwidthSharing, wmformat.iwmprofile3_createnewbandwidthsharing, wmsdkidl/IWMProfile3::CreateNewBandwidthSharing
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
 - IWMProfile3::CreateNewBandwidthSharing
 - wmsdkidl/IWMProfile3::CreateNewBandwidthSharing
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
 - IWMProfile3.CreateNewBandwidthSharing
---

# IWMProfile3::CreateNewBandwidthSharing


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>CreateNewBandwidthSharing</b> method creates a new bandwidth sharing object.

## -parameters

### -param ppBS [out]

Pointer to a variable that receives the address of the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing">IWMBandwidthSharing</a> interface of the new object.

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

To make use of the bandwidth sharing object, you must add it to the profile with a call to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing">AddBandwidthSharing</a>. A bandwidth sharing object cannot exist on its own. If you release the profile object without adding the bandwidth sharing object to the profile, you will lose the bandwidth sharing object.

You must configure the bandwidth sharing object before you use <b>AddBandwidthSharing</b> to include the bandwidth sharing object in the profile. For more information about configuring bandwidth sharing objects, see <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing">IWMBandwidthSharing Interface</a>.

## -see-also

<a href="/windows/desktop/wmformat/bandwidth-sharing-object">Bandwidth Sharing Object</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing">IWMBandwidthSharing Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing">IWMProfile3::AddBandwidthSharing</a>