---
UID: NF:wmsdkidl.IWMProfile.AddStream
title: IWMProfile::AddStream method
author: windows-driver-content
description: The AddStream method adds a stream to the profile by copying the stream configuration details into the profile.
old-location: wmformat\iwmprofile_addstream.htm
old-project: wmformat
ms.assetid: 3024fd2b-c261-49bd-b9a7-c1f43b31645b
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: AddStream method [windows Media Format], AddStream method [windows Media Format], IWMProfile interface, AddStream method [windows Media Format], IWMProfile2 interface, AddStream method [windows Media Format], IWMProfile3 interface, AddStream,IWMProfile.AddStream, IWMProfile, IWMProfile interface [windows Media Format], AddStream method, IWMProfile2 interface [windows Media Format], AddStream method, IWMProfile2::AddStream, IWMProfile3 interface [windows Media Format], AddStream method, IWMProfile3::AddStream, IWMProfile::AddStream, IWMProfileAddStream, wmformat.iwmprofile_addstream, wmsdkidl/IWMProfile2::AddStream, wmsdkidl/IWMProfile3::AddStream, wmsdkidl/IWMProfile::AddStream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmvcore.lib
-	Wmvcore.dll
-	WMStubDRM.lib
-	WMStubDRM.dll
-	qasf.dll
api_name:
-	IWMProfile.AddStream
-	IWMProfile2.AddStream
-	IWMProfile3.AddStream
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMProfile::AddStream method


## -description



The <b>AddStream</b> method adds a stream to the profile by copying the stream configuration details into the profile.



Use <b>AddStream</b> only to include a stream that is new to the profile. New streams can be created by calling <a href="https://msdn.microsoft.com/4a1478ff-00fb-46e2-97a3-e00e9c1b819a">IWMProfile::CreateNewStream</a>, but will not be added to the profile until <b>AddStream</b> is called.

If you edit an existing stream using <a href="https://msdn.microsoft.com/067c3f03-a79a-4693-b963-7081f79c72d3">IWMProfile::GetStream</a> or <a href="https://msdn.microsoft.com/507b1c55-1ecb-41dd-a6e5-298e1047a7ea">IWMProfile::GetStreamByNumber</a>, you should not call <b>AddStream</b> to include the changes. To include changes made to an existing stream, call <a href="https://msdn.microsoft.com/ac6de14b-b754-4f61-9f9a-656885641fbc">IWMProfile::ReconfigStream</a>.


## -parameters




### -param pConfig [in]

Pointer to the <a href="https://msdn.microsoft.com/e013996a-95b6-4cd3-9fb5-75dbce821eef">IWMStreamConfig</a> interface of the stream configuration object to be added to the profile. The stream must be configured by using the methods of the <b>IWMStreamConfig</b> interface before this method is used to add the stream to the profile.


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
The <i>pConfig</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough available memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed for an unspecified reason.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_STREAM</b></dt>
</dl>
</td>
<td width="60%">
The stream is not valid, possibly because it does not have a valid stream number.

</td>
</tr>
</table>
 




## -remarks



When a stream is added, its configuration is copied into the profile. A maximum of 63 streams can exist in a profile.




## -see-also




<a href="https://msdn.microsoft.com/00f28d6b-d27d-4268-960e-c8ea25e5359e">IWMProfile Interface</a>



<a href="https://msdn.microsoft.com/34e30edb-3247-4eaa-9a63-6d94c9e37c0b">IWMProfile2</a>



<a href="https://msdn.microsoft.com/7942aa81-ada7-4e9c-a261-f257f8f890b7">IWMProfile3</a>



<a href="https://msdn.microsoft.com/067c3f03-a79a-4693-b963-7081f79c72d3">IWMProfile::GetStream</a>



<a href="https://msdn.microsoft.com/82817b72-fde5-492e-b197-87bf145d0be9">IWMProfile::RemoveStream</a>



<a href="https://msdn.microsoft.com/e013996a-95b6-4cd3-9fb5-75dbce821eef">IWMStreamConfig Interface</a>
 

 

