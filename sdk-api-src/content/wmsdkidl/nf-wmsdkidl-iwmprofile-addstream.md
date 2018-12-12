---
UID: NF:wmsdkidl.IWMProfile.AddStream
title: IWMProfile::AddStream
author: windows-sdk-content
description: The AddStream method adds a stream to the profile by copying the stream configuration details into the profile.
old-location: wmformat\iwmprofile_addstream.htm
tech.root: wmformat
ms.assetid: 3024fd2b-c261-49bd-b9a7-c1f43b31645b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddStream, AddStream method [windows Media Format], AddStream method [windows Media Format],IWMProfile interface, AddStream method [windows Media Format],IWMProfile2 interface, AddStream method [windows Media Format],IWMProfile3 interface, IWMProfile interface [windows Media Format],AddStream method, IWMProfile.AddStream, IWMProfile2 interface [windows Media Format],AddStream method, IWMProfile2::AddStream, IWMProfile3 interface [windows Media Format],AddStream method, IWMProfile3::AddStream, IWMProfile::AddStream, IWMProfileAddStream, wmformat.iwmprofile_addstream, wmsdkidl/IWMProfile2::AddStream, wmsdkidl/IWMProfile3::AddStream, wmsdkidl/IWMProfile::AddStream
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
 - qasf.dll
api_name:
 - IWMProfile.AddStream
 - IWMProfile2.AddStream
 - IWMProfile3.AddStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMProfile::AddStream


## -description



The <b>AddStream</b> method adds a stream to the profile by copying the stream configuration details into the profile.



Use <b>AddStream</b> only to include a stream that is new to the profile. New streams can be created by calling <a href="https://msdn.microsoft.com/en-us/library/Dd757401(v=VS.85).aspx">IWMProfile::CreateNewStream</a>, but will not be added to the profile until <b>AddStream</b> is called.

If you edit an existing stream using <a href="https://msdn.microsoft.com/en-us/library/Dd757406(v=VS.85).aspx">IWMProfile::GetStream</a> or <a href="https://msdn.microsoft.com/en-us/library/Dd757407(v=VS.85).aspx">IWMProfile::GetStreamByNumber</a>, you should not call <b>AddStream</b> to include the changes. To include changes made to an existing stream, call <a href="https://msdn.microsoft.com/en-us/library/Dd757410(v=VS.85).aspx">IWMProfile::ReconfigStream</a>.


## -parameters




### -param pConfig [in]

Pointer to the <a href="https://msdn.microsoft.com/en-us/library/Dd798546(v=VS.85).aspx">IWMStreamConfig</a> interface of the stream configuration object to be added to the profile. The stream must be configured by using the methods of the <b>IWMStreamConfig</b> interface before this method is used to add the stream to the profile.


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



<a href="https://msdn.microsoft.com/en-us/library/Dd757266(v=VS.85).aspx">IWMProfile2</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757268(v=VS.85).aspx">IWMProfile3</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757406(v=VS.85).aspx">IWMProfile::GetStream</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757412(v=VS.85).aspx">IWMProfile::RemoveStream</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd798546(v=VS.85).aspx">IWMStreamConfig Interface</a>
 

 

