---
UID: NF:wmsdkidl.IWMProfile.GetStreamByNumber
title: IWMProfile::GetStreamByNumber (wmsdkidl.h)
description: The GetStreamByNumber method retrieves a stream from the profile.helpviewer_keywords: ["GetStreamByNumber","GetStreamByNumber method [windows Media Format]","GetStreamByNumber method [windows Media Format]","IWMProfile interface","GetStreamByNumber method [windows Media Format]","IWMProfile2 interface","GetStreamByNumber method [windows Media Format]","IWMProfile3 interface","IWMProfile interface [windows Media Format]","GetStreamByNumber method","IWMProfile.GetStreamByNumber","IWMProfile2 interface [windows Media Format]","GetStreamByNumber method","IWMProfile2::GetStreamByNumber","IWMProfile3 interface [windows Media Format]","GetStreamByNumber method","IWMProfile3::GetStreamByNumber","IWMProfile::GetStreamByNumber","IWMProfileGetStreamByNumber","wmformat.iwmprofile_getstreambynumber","wmsdkidl/IWMProfile2::GetStreamByNumber","wmsdkidl/IWMProfile3::GetStreamByNumber","wmsdkidl/IWMProfile::GetStreamByNumber"]
old-location: wmformat\iwmprofile_getstreambynumber.htm
tech.root: wmformat
ms.assetid: 507b1c55-1ecb-41dd-a6e5-298e1047a7ea
ms.date: 12/05/2018
ms.keywords: GetStreamByNumber, GetStreamByNumber method [windows Media Format], GetStreamByNumber method [windows Media Format],IWMProfile interface, GetStreamByNumber method [windows Media Format],IWMProfile2 interface, GetStreamByNumber method [windows Media Format],IWMProfile3 interface, IWMProfile interface [windows Media Format],GetStreamByNumber method, IWMProfile.GetStreamByNumber, IWMProfile2 interface [windows Media Format],GetStreamByNumber method, IWMProfile2::GetStreamByNumber, IWMProfile3 interface [windows Media Format],GetStreamByNumber method, IWMProfile3::GetStreamByNumber, IWMProfile::GetStreamByNumber, IWMProfileGetStreamByNumber, wmformat.iwmprofile_getstreambynumber, wmsdkidl/IWMProfile2::GetStreamByNumber, wmsdkidl/IWMProfile3::GetStreamByNumber, wmsdkidl/IWMProfile::GetStreamByNumber
f1_keywords:
- wmsdkidl/IWMProfile.GetStreamByNumber
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
- IWMProfile.GetStreamByNumber
- IWMProfile2.GetStreamByNumber
- IWMProfile3.GetStreamByNumber
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMProfile::GetStreamByNumber


## -description



The <b>GetStreamByNumber</b> method retrieves a stream from the profile.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number.


### -param ppConfig [out]

Pointer to a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig">IWMStreamConfig</a> interface of the stream configuration object that describes the specified stream.


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
The <i>ppConfig</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_NO_STREAM</b></dt>
</dl>
</td>
<td width="60%">
The <i>wStreamNum</i> parameter is not valid.

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
</table>
 




## -remarks



Stream numbers are in the range of 1 through 63.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/iwmprofile">IWMProfile Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2">IWMProfile2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstream">IWMProfile::GetStream</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-removestreambynumber">IWMProfile::RemoveStreamByNumber</a>
 

 

