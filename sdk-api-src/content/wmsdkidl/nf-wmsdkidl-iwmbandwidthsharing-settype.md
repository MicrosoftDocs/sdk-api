---
UID: NF:wmsdkidl.IWMBandwidthSharing.SetType
title: IWMBandwidthSharing::SetType (wmsdkidl.h)
description: The SetType method sets the type of sharing (exclusive or partial) for the bandwidth sharing object.
helpviewer_keywords: ["IWMBandwidthSharing interface [windows Media Format]","SetType method","IWMBandwidthSharing.SetType","IWMBandwidthSharing::SetType","IWMBandwidthSharingSetType","SetType","SetType method [windows Media Format]","SetType method [windows Media Format]","IWMBandwidthSharing interface","wmformat.iwmbandwidthsharing_settype","wmsdkidl/IWMBandwidthSharing::SetType"]
old-location: wmformat\iwmbandwidthsharing_settype.htm
tech.root: wmformat
ms.assetid: 3f4fc06a-ffbe-4854-8e64-d369acfac271
ms.date: 12/05/2018
ms.keywords: IWMBandwidthSharing interface [windows Media Format],SetType method, IWMBandwidthSharing.SetType, IWMBandwidthSharing::SetType, IWMBandwidthSharingSetType, SetType, SetType method [windows Media Format], SetType method [windows Media Format],IWMBandwidthSharing interface, wmformat.iwmbandwidthsharing_settype, wmsdkidl/IWMBandwidthSharing::SetType
f1_keywords:
- wmsdkidl/IWMBandwidthSharing.SetType
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
- IWMBandwidthSharing.SetType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMBandwidthSharing::SetType


## -description



The <b>SetType</b> method sets the type of sharing (exclusive or partial) for the bandwidth sharing object.




## -parameters




### -param guidType [in]

Globally unique identifier specifying the type of combined stream to be used. The only valid GUIDs are those in the following table.

<table>
<tr>
<th>Bandwidth sharing type
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>CLSID_WMBandwidthSharing_Exclusive</td>
<td>Only one of the constituent streams can be active at any given time.</td>
</tr>
<tr>
<td>CLSID_WMBandwidthSharing_Partial</td>
<td>The constituent streams can be active simultaneously.</td>
</tr>
</table>
 


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
The GUID passed in <i>guidType</i> is any value other than CLSID_BandwidthSharingExclusive or CLSID_BandwidthSharingPartial.

</td>
</tr>
</table>
 




## -remarks



The settings of a bandwidth sharing object are purely informational. They are not checked for accuracy.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing">IWMBandwidthSharing Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmbandwidthsharing-gettype">IWMBandwidthSharing::GetType</a>
 

 

