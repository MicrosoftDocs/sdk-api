---
UID: NF:wmsdkidl.IWMProfile3.AddBandwidthSharing
title: IWMProfile3::AddBandwidthSharing
author: windows-sdk-content
description: The AddBandwidthSharing method adds an existing bandwidth sharing object to the profile. Bandwidth sharing objects are created with a call to CreateNewBandwidthSharing. You must configure the bandwidth sharing object before adding it to the profile.
old-location: wmformat\iwmprofile3_addbandwidthsharing.htm
tech.root: wmformat
ms.assetid: 174a4583-93fb-41cd-ba14-a959a28c1ea3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddBandwidthSharing, AddBandwidthSharing method [windows Media Format], AddBandwidthSharing method [windows Media Format],IWMProfile3 interface, IWMProfile3 interface [windows Media Format],AddBandwidthSharing method, IWMProfile3.AddBandwidthSharing, IWMProfile3::AddBandwidthSharing, IWMProfile3AddBandwidthSharing, wmformat.iwmprofile3_addbandwidthsharing, wmsdkidl/IWMProfile3::AddBandwidthSharing
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWMProfile3.AddBandwidthSharing
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMProfile3::AddBandwidthSharing


## -description



The <b>AddBandwidthSharing</b> method adds an existing bandwidth sharing object to the profile. Bandwidth sharing objects are created with a call to <a href="https://msdn.microsoft.com/en-us/library/Dd757270(v=VS.85).aspx">CreateNewBandwidthSharing</a>. You must configure the bandwidth sharing object before adding it to the profile.




## -parameters




### -param pBS [in]

Pointer to the <a href="https://msdn.microsoft.com/en-us/library/Dd743298(v=VS.85).aspx">IWMBandwidthSharing</a> interface of a bandwidth sharing object.


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




<a href="https://msdn.microsoft.com/9dc863da-1842-41e7-b66c-c97e0140046d">Bandwidth Sharing Object</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757268(v=VS.85).aspx">IWMProfile3 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757272(v=VS.85).aspx">IWMProfile3::GetBandwidthSharing</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757381(v=VS.85).aspx">IWMProfile3::RemoveBandwidthSharing</a>
 

 

