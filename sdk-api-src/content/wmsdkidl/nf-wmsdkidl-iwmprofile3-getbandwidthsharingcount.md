---
UID: NF:wmsdkidl.IWMProfile3.GetBandwidthSharingCount
title: IWMProfile3::GetBandwidthSharingCount (wmsdkidl.h)
description: The GetBandwidthSharingCount method retrieves the total number of bandwidth sharing objects that have been added to the profile.
helpviewer_keywords: ["GetBandwidthSharingCount","GetBandwidthSharingCount method [windows Media Format]","GetBandwidthSharingCount method [windows Media Format]","IWMProfile3 interface","IWMProfile3 interface [windows Media Format]","GetBandwidthSharingCount method","IWMProfile3.GetBandwidthSharingCount","IWMProfile3::GetBandwidthSharingCount","IWMProfile3GetBandwidthSharingCount","wmformat.iwmprofile3_getbandwidthsharingcount","wmsdkidl/IWMProfile3::GetBandwidthSharingCount"]
old-location: wmformat\iwmprofile3_getbandwidthsharingcount.htm
tech.root: wmformat
ms.assetid: 7f5a11a7-d81a-4ca1-8b0f-1d561f736523
ms.date: 12/05/2018
ms.keywords: GetBandwidthSharingCount, GetBandwidthSharingCount method [windows Media Format], GetBandwidthSharingCount method [windows Media Format],IWMProfile3 interface, IWMProfile3 interface [windows Media Format],GetBandwidthSharingCount method, IWMProfile3.GetBandwidthSharingCount, IWMProfile3::GetBandwidthSharingCount, IWMProfile3GetBandwidthSharingCount, wmformat.iwmprofile3_getbandwidthsharingcount, wmsdkidl/IWMProfile3::GetBandwidthSharingCount
f1_keywords:
- wmsdkidl/IWMProfile3.GetBandwidthSharingCount
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
- IWMProfile3.GetBandwidthSharingCount
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMProfile3::GetBandwidthSharingCount


## -description



The <b>GetBandwidthSharingCount</b> method retrieves the total number of bandwidth sharing objects that have been added to the profile.




## -parameters




### -param pcBS [out]

Pointer to receive the total number of bandwidth sharing objects.


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
<i>pcBS</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/bandwidth-sharing-object">Bandwidth Sharing Object</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing">IWMProfile3::GetBandwidthSharing</a>
 

 

