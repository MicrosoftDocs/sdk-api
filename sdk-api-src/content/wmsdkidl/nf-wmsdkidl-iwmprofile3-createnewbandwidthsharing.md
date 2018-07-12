---
UID: NF:wmsdkidl.IWMProfile3.CreateNewBandwidthSharing
title: IWMProfile3::CreateNewBandwidthSharing
author: windows-sdk-content
description: The CreateNewBandwidthSharing method creates a new bandwidth sharing object.
old-location: wmformat\iwmprofile3_createnewbandwidthsharing.htm
old-project: wmformat
ms.assetid: ab6c9903-95ea-499b-be75-ff57328336f0
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: CreateNewBandwidthSharing, CreateNewBandwidthSharing method [windows Media Format], CreateNewBandwidthSharing method [windows Media Format],IWMProfile3 interface, IWMProfile3 interface [windows Media Format],CreateNewBandwidthSharing method, IWMProfile3.CreateNewBandwidthSharing, IWMProfile3::CreateNewBandwidthSharing, IWMProfile3CreateNewBandwidthSharing, wmformat.iwmprofile3_createnewbandwidthsharing, wmsdkidl/IWMProfile3::CreateNewBandwidthSharing
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
 - IWMProfile3.CreateNewBandwidthSharing
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMProfile3::CreateNewBandwidthSharing


## -description



The <b>CreateNewBandwidthSharing</b> method creates a new bandwidth sharing object.




## -parameters




### -param ppBS [out]

Pointer to a variable that receives the address of the <a href="https://msdn.microsoft.com/fd0e48bb-2e5e-4158-9ff1-5b603f219689">IWMBandwidthSharing</a> interface of the new object.


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



To make use of the bandwidth sharing object, you must add it to the profile with a call to <a href="https://msdn.microsoft.com/174a4583-93fb-41cd-ba14-a959a28c1ea3">AddBandwidthSharing</a>. A bandwidth sharing object cannot exist on its own. If you release the profile object without adding the bandwidth sharing object to the profile, you will lose the bandwidth sharing object.

You must configure the bandwidth sharing object before you use <b>AddBandwidthSharing</b> to include the bandwidth sharing object in the profile. For more information about configuring bandwidth sharing objects, see <a href="https://msdn.microsoft.com/fd0e48bb-2e5e-4158-9ff1-5b603f219689">IWMBandwidthSharing Interface</a>.




## -see-also




<a href="https://msdn.microsoft.com/9dc863da-1842-41e7-b66c-c97e0140046d">Bandwidth Sharing Object</a>



<a href="https://msdn.microsoft.com/fd0e48bb-2e5e-4158-9ff1-5b603f219689">IWMBandwidthSharing Interface</a>



<a href="https://msdn.microsoft.com/7942aa81-ada7-4e9c-a261-f257f8f890b7">IWMProfile3 Interface</a>



<a href="https://msdn.microsoft.com/174a4583-93fb-41cd-ba14-a959a28c1ea3">IWMProfile3::AddBandwidthSharing</a>
 

 

