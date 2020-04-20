---
UID: NF:wmsdkidl.IWMProfile3.GetBandwidthSharing
title: IWMProfile3::GetBandwidthSharing (wmsdkidl.h)
description: The GetBandwidthSharing method retrieves a bandwidth sharing object from a profile.helpviewer_keywords: ["GetBandwidthSharing","GetBandwidthSharing method [windows Media Format]","GetBandwidthSharing method [windows Media Format]","IWMProfile3 interface","IWMProfile3 interface [windows Media Format]","GetBandwidthSharing method","IWMProfile3.GetBandwidthSharing","IWMProfile3::GetBandwidthSharing","IWMProfile3GetBandwidthSharing","wmformat.iwmprofile3_getbandwidthsharing","wmsdkidl/IWMProfile3::GetBandwidthSharing"]
old-location: wmformat\iwmprofile3_getbandwidthsharing.htm
tech.root: wmformat
ms.assetid: be66ff8b-c883-4329-aaa4-e9549d0cbb9e
ms.date: 12/05/2018
ms.keywords: GetBandwidthSharing, GetBandwidthSharing method [windows Media Format], GetBandwidthSharing method [windows Media Format],IWMProfile3 interface, IWMProfile3 interface [windows Media Format],GetBandwidthSharing method, IWMProfile3.GetBandwidthSharing, IWMProfile3::GetBandwidthSharing, IWMProfile3GetBandwidthSharing, wmformat.iwmprofile3_getbandwidthsharing, wmsdkidl/IWMProfile3::GetBandwidthSharing
f1_keywords:
- wmsdkidl/IWMProfile3.GetBandwidthSharing
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMProfile3::GetBandwidthSharing


## -description



The <b>GetBandwidthSharing</b> method retrieves a bandwidth sharing object from a profile.




## -parameters




### -param dwBSIndex [in]

<b>DWORD</b> containing the index number of the bandwidth sharing object you want to retrieve.


### -param ppBS [out]

Pointer to receive the address of the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing">IWMBandwidthSharing</a> interface of the object requested.


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




<a href="https://docs.microsoft.com/windows/desktop/wmformat/bandwidth-sharing-object">Bandwidth Sharing Object</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing">IWMProfile3::AddBandwidthSharing</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharingcount">IWMProfile3::GetBandwidthSharingCount</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-removebandwidthsharing">IWMProfile3::RemoveBandwidthSharing</a>
 

 

