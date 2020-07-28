---
UID: NF:wmsdkidl.IWMProfile.ReconfigStream
title: IWMProfile::ReconfigStream (wmsdkidl.h)
description: The ReconfigStream method enables changes made to a stream configuration to be included in the profile. Use this method when you have made changes to a stream that has already been included in the profile.
helpviewer_keywords: ["IWMProfile interface [windows Media Format]","ReconfigStream method","IWMProfile.ReconfigStream","IWMProfile2 interface [windows Media Format]","ReconfigStream method","IWMProfile2::ReconfigStream","IWMProfile3 interface [windows Media Format]","ReconfigStream method","IWMProfile3::ReconfigStream","IWMProfile::ReconfigStream","IWMProfileReconfigStream","ReconfigStream","ReconfigStream method [windows Media Format]","ReconfigStream method [windows Media Format]","IWMProfile interface","ReconfigStream method [windows Media Format]","IWMProfile2 interface","ReconfigStream method [windows Media Format]","IWMProfile3 interface","wmformat.iwmprofile_reconfigstream","wmsdkidl/IWMProfile2::ReconfigStream","wmsdkidl/IWMProfile3::ReconfigStream","wmsdkidl/IWMProfile::ReconfigStream"]
old-location: wmformat\iwmprofile_reconfigstream.htm
tech.root: wmformat
ms.assetid: ac6de14b-b754-4f61-9f9a-656885641fbc
ms.date: 12/05/2018
ms.keywords: IWMProfile interface [windows Media Format],ReconfigStream method, IWMProfile.ReconfigStream, IWMProfile2 interface [windows Media Format],ReconfigStream method, IWMProfile2::ReconfigStream, IWMProfile3 interface [windows Media Format],ReconfigStream method, IWMProfile3::ReconfigStream, IWMProfile::ReconfigStream, IWMProfileReconfigStream, ReconfigStream, ReconfigStream method [windows Media Format], ReconfigStream method [windows Media Format],IWMProfile interface, ReconfigStream method [windows Media Format],IWMProfile2 interface, ReconfigStream method [windows Media Format],IWMProfile3 interface, wmformat.iwmprofile_reconfigstream, wmsdkidl/IWMProfile2::ReconfigStream, wmsdkidl/IWMProfile3::ReconfigStream, wmsdkidl/IWMProfile::ReconfigStream
f1_keywords:
- wmsdkidl/IWMProfile.ReconfigStream
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
- IWMProfile.ReconfigStream
- IWMProfile2.ReconfigStream
- IWMProfile3.ReconfigStream
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMProfile::ReconfigStream


## -description



The <b>ReconfigStream</b> method enables changes made to a stream configuration to be included in the profile. Use this method when you have made changes to a stream that has already been included in the profile.




## -parameters




### -param pConfig [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig">IWMStreamConfig</a> interface of the stream configuration object for the stream you want to reconfigure.


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
<dt><b>E_UNEXPECTED</b></dt>
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
The method is working on a stream that is <b>NULL</b> or not valid.

</td>
</tr>
</table>
 




## -remarks



You can call either <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstream">IWMProfile::GetStream</a> or <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber">IWMProfile::GetStreamByNumber</a> to retrieve a stream already added to a profile.

If you create a new stream by calling <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream">IWMProfile::CreateNewStream</a>, you must call <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-addstream">IWMProfile::AddStream</a> to include it in the profile. Calling <b>ReconfigStream</b> on a new stream will result in an error.

Updating a stream configuration object has no effect on the profile until the application calls <b>ReconfigStream</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/iwmprofile">IWMProfile Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2">IWMProfile2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3</a>
 

 

