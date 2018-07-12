---
UID: NF:wmsdkidl.IWMBandwidthSharing.SetType
title: IWMBandwidthSharing::SetType
author: windows-sdk-content
description: The SetType method sets the type of sharing (exclusive or partial) for the bandwidth sharing object.
old-location: wmformat\iwmbandwidthsharing_settype.htm
old-project: wmformat
ms.assetid: 3f4fc06a-ffbe-4854-8e64-d369acfac271
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: IWMBandwidthSharing interface [windows Media Format],SetType method, IWMBandwidthSharing.SetType, IWMBandwidthSharing::SetType, IWMBandwidthSharingSetType, SetType, SetType method [windows Media Format], SetType method [windows Media Format],IWMBandwidthSharing interface, wmformat.iwmbandwidthsharing_settype, wmsdkidl/IWMBandwidthSharing::SetType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WM_AETYPE
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
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMBandwidthSharing::SetType


## -description



The <b>SetType</b> method sets the type of sharing (exclusive or partial) for the bandwidth sharing object.




## -parameters




### -param guidType [in]

Globally unique identifier specifying the type of combined stream to be used. The only valid GUIDs are those in the following table.

<table>
<tr>
<th>
                  Bandwidth sharing type
                </th>
<th>
                  Description
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




<a href="https://msdn.microsoft.com/fd0e48bb-2e5e-4158-9ff1-5b603f219689">IWMBandwidthSharing Interface</a>



<a href="https://msdn.microsoft.com/acef383f-83cb-45be-80fa-1339b391f32b">IWMBandwidthSharing::GetType</a>
 

 

