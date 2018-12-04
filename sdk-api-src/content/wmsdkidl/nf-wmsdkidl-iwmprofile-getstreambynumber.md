---
UID: NF:wmsdkidl.IWMProfile.GetStreamByNumber
title: IWMProfile::GetStreamByNumber
author: windows-sdk-content
description: The GetStreamByNumber method retrieves a stream from the profile.
old-location: wmformat\iwmprofile_getstreambynumber.htm
tech.root: wmformat
ms.assetid: 507b1c55-1ecb-41dd-a6e5-298e1047a7ea
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetStreamByNumber, GetStreamByNumber method [windows Media Format], GetStreamByNumber method [windows Media Format],IWMProfile interface, GetStreamByNumber method [windows Media Format],IWMProfile2 interface, GetStreamByNumber method [windows Media Format],IWMProfile3 interface, IWMProfile interface [windows Media Format],GetStreamByNumber method, IWMProfile.GetStreamByNumber, IWMProfile2 interface [windows Media Format],GetStreamByNumber method, IWMProfile2::GetStreamByNumber, IWMProfile3 interface [windows Media Format],GetStreamByNumber method, IWMProfile3::GetStreamByNumber, IWMProfile::GetStreamByNumber, IWMProfileGetStreamByNumber, wmformat.iwmprofile_getstreambynumber, wmsdkidl/IWMProfile2::GetStreamByNumber, wmsdkidl/IWMProfile3::GetStreamByNumber, wmsdkidl/IWMProfile::GetStreamByNumber
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
 - IWMProfile.GetStreamByNumber
 - IWMProfile2.GetStreamByNumber
 - IWMProfile3.GetStreamByNumber
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMProfile::GetStreamByNumber


## -description



The <b>GetStreamByNumber</b> method retrieves a stream from the profile.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number.


### -param ppConfig [out]

Pointer to a pointer to the <a href="https://msdn.microsoft.com/e013996a-95b6-4cd3-9fb5-75dbce821eef">IWMStreamConfig</a> interface of the stream configuration object that describes the specified stream.


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




<a href="https://msdn.microsoft.com/00f28d6b-d27d-4268-960e-c8ea25e5359e">IWMProfile Interface</a>



<a href="https://msdn.microsoft.com/34e30edb-3247-4eaa-9a63-6d94c9e37c0b">IWMProfile2</a>



<a href="https://msdn.microsoft.com/7942aa81-ada7-4e9c-a261-f257f8f890b7">IWMProfile3</a>



<a href="https://msdn.microsoft.com/067c3f03-a79a-4693-b963-7081f79c72d3">IWMProfile::GetStream</a>



<a href="https://msdn.microsoft.com/72ecc794-d393-416e-bc21-5a7756e76d99">IWMProfile::RemoveStreamByNumber</a>
 

 

