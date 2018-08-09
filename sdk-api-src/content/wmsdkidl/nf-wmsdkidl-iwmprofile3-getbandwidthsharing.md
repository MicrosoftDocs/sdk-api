---
UID: NF:wmsdkidl.IWMProfile3.GetBandwidthSharing
title: IWMProfile3::GetBandwidthSharing
author: windows-sdk-content
description: The GetBandwidthSharing method retrieves a bandwidth sharing object from a profile.
old-location: wmformat\iwmprofile3_getbandwidthsharing.htm
old-project: wmformat
ms.assetid: be66ff8b-c883-4329-aaa4-e9549d0cbb9e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetBandwidthSharing, GetBandwidthSharing method [windows Media Format], GetBandwidthSharing method [windows Media Format],IWMProfile3 interface, IWMProfile3 interface [windows Media Format],GetBandwidthSharing method, IWMProfile3.GetBandwidthSharing, IWMProfile3::GetBandwidthSharing, IWMProfile3GetBandwidthSharing, wmformat.iwmprofile3_getbandwidthsharing, wmsdkidl/IWMProfile3::GetBandwidthSharing
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
 - IWMProfile3.GetBandwidthSharing
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMProfile3::GetBandwidthSharing


## -description



The <b>GetBandwidthSharing</b> method retrieves a bandwidth sharing object from a profile.




## -parameters




### -param dwBSIndex [in]

<b>DWORD</b> containing the index number of the bandwidth sharing object you want to retrieve.


### -param ppBS [out]

Pointer to receive the address of the <a href="https://msdn.microsoft.com/fd0e48bb-2e5e-4158-9ff1-5b603f219689">IWMBandwidthSharing</a> interface of the object requested.


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




<a href="https://msdn.microsoft.com/9dc863da-1842-41e7-b66c-c97e0140046d">Bandwidth Sharing Object</a>



<a href="https://msdn.microsoft.com/7942aa81-ada7-4e9c-a261-f257f8f890b7">IWMProfile3 Interface</a>



<a href="https://msdn.microsoft.com/174a4583-93fb-41cd-ba14-a959a28c1ea3">IWMProfile3::AddBandwidthSharing</a>



<a href="https://msdn.microsoft.com/7f5a11a7-d81a-4ca1-8b0f-1d561f736523">IWMProfile3::GetBandwidthSharingCount</a>



<a href="https://msdn.microsoft.com/3c0a90aa-154a-49c9-ab8e-0d1c4ce02641">IWMProfile3::RemoveBandwidthSharing</a>
 

 

