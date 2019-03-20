---
UID: NF:wmsdkidl.IWMProfile.RemoveStream
title: IWMProfile::RemoveStream (wmsdkidl.h)
author: windows-sdk-content
description: The RemoveStream method removes a stream from the profile.
old-location: wmformat\iwmprofile_removestream.htm
tech.root: wmformat
ms.assetid: 82817b72-fde5-492e-b197-87bf145d0be9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMProfile interface [windows Media Format],RemoveStream method, IWMProfile.RemoveStream, IWMProfile2 interface [windows Media Format],RemoveStream method, IWMProfile2::RemoveStream, IWMProfile3 interface [windows Media Format],RemoveStream method, IWMProfile3::RemoveStream, IWMProfile::RemoveStream, IWMProfileRemoveStream, RemoveStream, RemoveStream method [windows Media Format], RemoveStream method [windows Media Format],IWMProfile interface, RemoveStream method [windows Media Format],IWMProfile2 interface, RemoveStream method [windows Media Format],IWMProfile3 interface, wmformat.iwmprofile_removestream, wmsdkidl/IWMProfile2::RemoveStream, wmsdkidl/IWMProfile3::RemoveStream, wmsdkidl/IWMProfile::RemoveStream
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
 - IWMProfile.RemoveStream
 - IWMProfile2.RemoveStream
 - IWMProfile3.RemoveStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMProfile::RemoveStream


## -description



The <b>RemoveStream</b> method removes a stream from the profile.




## -parameters




### -param pConfig [in]

Pointer to the <a href="https://msdn.microsoft.com/en-us/library/Dd798546(v=VS.85).aspx">IWMStreamConfig</a> interface of the stream configuration object that describes the stream you want to remove.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pConfig</i> parameter is <b>NULL</b> or not valid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/00f28d6b-d27d-4268-960e-c8ea25e5359e">IWMProfile Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757266(v=VS.85).aspx">IWMProfile2</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757268(v=VS.85).aspx">IWMProfile3</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757399(v=VS.85).aspx">IWMProfile::AddStream</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757413(v=VS.85).aspx">IWMProfile::RemoveStreamByNumber</a>
 

 

