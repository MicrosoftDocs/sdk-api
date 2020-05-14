---
UID: NF:wmsdkidl.IWMProfile3.RemoveBandwidthSharing
title: IWMProfile3::RemoveBandwidthSharing (wmsdkidl.h)
description: The RemoveBandwidthSharing method removes a bandwidth sharing object from the profile.helpviewer_keywords: ["IWMProfile3 interface [windows Media Format]","RemoveBandwidthSharing method","IWMProfile3.RemoveBandwidthSharing","IWMProfile3::RemoveBandwidthSharing","IWMProfile3RemoveBandwidthSharing","RemoveBandwidthSharing","RemoveBandwidthSharing method [windows Media Format]","RemoveBandwidthSharing method [windows Media Format]","IWMProfile3 interface","wmformat.iwmprofile3_removebandwidthsharing","wmsdkidl/IWMProfile3::RemoveBandwidthSharing"]
old-location: wmformat\iwmprofile3_removebandwidthsharing.htm
tech.root: wmformat
ms.assetid: 3c0a90aa-154a-49c9-ab8e-0d1c4ce02641
ms.date: 12/05/2018
ms.keywords: IWMProfile3 interface [windows Media Format],RemoveBandwidthSharing method, IWMProfile3.RemoveBandwidthSharing, IWMProfile3::RemoveBandwidthSharing, IWMProfile3RemoveBandwidthSharing, RemoveBandwidthSharing, RemoveBandwidthSharing method [windows Media Format], RemoveBandwidthSharing method [windows Media Format],IWMProfile3 interface, wmformat.iwmprofile3_removebandwidthsharing, wmsdkidl/IWMProfile3::RemoveBandwidthSharing
f1_keywords:
- wmsdkidl/IWMProfile3.RemoveBandwidthSharing
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
- IWMProfile3.RemoveBandwidthSharing
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMProfile3::RemoveBandwidthSharing


## -description



The <b>RemoveBandwidthSharing</b> method removes a bandwidth sharing object from the profile. If you do not already have a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing">IWMBandwidthSharing</a> interface of the object you want to remove, you must obtain one with a call to <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing">IWMProfile3::GetBandwidthSharing</a>.




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




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing">IWMProfile3::AddBandwidthSharing</a>
 

 

