---
UID: NF:wmsdkidl.IWMProfile.AddStream
title: IWMProfile::AddStream (wmsdkidl.h)
description: The AddStream method adds a stream to the profile by copying the stream configuration details into the profile.
helpviewer_keywords: ["AddStream","AddStream method [windows Media Format]","AddStream method [windows Media Format]","IWMProfile interface","AddStream method [windows Media Format]","IWMProfile2 interface","AddStream method [windows Media Format]","IWMProfile3 interface","IWMProfile interface [windows Media Format]","AddStream method","IWMProfile.AddStream","IWMProfile2 interface [windows Media Format]","AddStream method","IWMProfile2::AddStream","IWMProfile3 interface [windows Media Format]","AddStream method","IWMProfile3::AddStream","IWMProfile::AddStream","IWMProfileAddStream","wmformat.iwmprofile_addstream","wmsdkidl/IWMProfile2::AddStream","wmsdkidl/IWMProfile3::AddStream","wmsdkidl/IWMProfile::AddStream"]
old-location: wmformat\iwmprofile_addstream.htm
tech.root: wmformat
ms.assetid: 3024fd2b-c261-49bd-b9a7-c1f43b31645b
ms.date: 12/05/2018
ms.keywords: AddStream, AddStream method [windows Media Format], AddStream method [windows Media Format],IWMProfile interface, AddStream method [windows Media Format],IWMProfile2 interface, AddStream method [windows Media Format],IWMProfile3 interface, IWMProfile interface [windows Media Format],AddStream method, IWMProfile.AddStream, IWMProfile2 interface [windows Media Format],AddStream method, IWMProfile2::AddStream, IWMProfile3 interface [windows Media Format],AddStream method, IWMProfile3::AddStream, IWMProfile::AddStream, IWMProfileAddStream, wmformat.iwmprofile_addstream, wmsdkidl/IWMProfile2::AddStream, wmsdkidl/IWMProfile3::AddStream, wmsdkidl/IWMProfile::AddStream
f1_keywords:
- wmsdkidl/IWMProfile.AddStream
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMProfile::AddStream


## -description



The <b>AddStream</b> method adds a stream to the profile by copying the stream configuration details into the profile.



Use <b>AddStream</b> only to include a stream that is new to the profile. New streams can be created by calling <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream">IWMProfile::CreateNewStream</a>, but will not be added to the profile until <b>AddStream</b> is called.

If you edit an existing stream using <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstream">IWMProfile::GetStream</a> or <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber">IWMProfile::GetStreamByNumber</a>, you should not call <b>AddStream</b> to include the changes. To include changes made to an existing stream, call <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream">IWMProfile::ReconfigStream</a>.


## -parameters




### -param pConfig [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig">IWMStreamConfig</a> interface of the stream configuration object to be added to the profile. The stream must be configured by using the methods of the <b>IWMStreamConfig</b> interface before this method is used to add the stream to the profile.


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




<a href="https://docs.microsoft.com/windows/desktop/wmformat/iwmprofile">IWMProfile Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2">IWMProfile2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstream">IWMProfile::GetStream</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-removestream">IWMProfile::RemoveStream</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig">IWMStreamConfig Interface</a>
 

 

