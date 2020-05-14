---
UID: NF:wmsdkidl.IWMBandwidthSharing.GetType
title: IWMBandwidthSharing::GetType (wmsdkidl.h)
description: The GetType method retrieves the type of sharing for the bandwidth sharing object.helpviewer_keywords: ["GetType","GetType method [windows Media Format]","GetType method [windows Media Format]","IWMBandwidthSharing interface","IWMBandwidthSharing interface [windows Media Format]","GetType method","IWMBandwidthSharing.GetType","IWMBandwidthSharing::GetType","IWMBandwidthSharingGetType","wmformat.iwmbandwidthsharing_gettype","wmsdkidl/IWMBandwidthSharing::GetType"]
old-location: wmformat\iwmbandwidthsharing_gettype.htm
tech.root: wmformat
ms.assetid: acef383f-83cb-45be-80fa-1339b391f32b
ms.date: 12/05/2018
ms.keywords: GetType, GetType method [windows Media Format], GetType method [windows Media Format],IWMBandwidthSharing interface, IWMBandwidthSharing interface [windows Media Format],GetType method, IWMBandwidthSharing.GetType, IWMBandwidthSharing::GetType, IWMBandwidthSharingGetType, wmformat.iwmbandwidthsharing_gettype, wmsdkidl/IWMBandwidthSharing::GetType
f1_keywords:
- wmsdkidl/IWMBandwidthSharing.GetType
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
- IWMBandwidthSharing.GetType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMBandwidthSharing::GetType


## -description



The <b>GetType</b> method retrieves the type of sharing for the bandwidth sharing object.




## -parameters




### -param pguidType [out]

Pointer to a globally unique identifier specifying the type of combined stream to be used. This will be one of the following values.

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
The pointer passed is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The settings of a bandwidth sharing object are purely informational. They are not checked for accuracy.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing">IWMBandwidthSharing Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmbandwidthsharing-settype">IWMBandwidthSharing::SetType</a>
 

 

