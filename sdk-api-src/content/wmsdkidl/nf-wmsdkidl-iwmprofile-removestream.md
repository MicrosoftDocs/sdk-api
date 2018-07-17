---
UID: NF:wmsdkidl.IWMProfile.RemoveStream
title: IWMProfile::RemoveStream
author: windows-sdk-content
description: The RemoveStream method removes a stream from the profile.
old-location: wmformat\iwmprofile_removestream.htm
old-project: wmformat
ms.assetid: 82817b72-fde5-492e-b197-87bf145d0be9
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IWMProfile interface [windows Media Format],RemoveStream method, IWMProfile.RemoveStream, IWMProfile2 interface [windows Media Format],RemoveStream method, IWMProfile2::RemoveStream, IWMProfile3 interface [windows Media Format],RemoveStream method, IWMProfile3::RemoveStream, IWMProfile::RemoveStream, IWMProfileRemoveStream, RemoveStream, RemoveStream method [windows Media Format], RemoveStream method [windows Media Format],IWMProfile interface, RemoveStream method [windows Media Format],IWMProfile2 interface, RemoveStream method [windows Media Format],IWMProfile3 interface, wmformat.iwmprofile_removestream, wmsdkidl/IWMProfile2::RemoveStream, wmsdkidl/IWMProfile3::RemoveStream, wmsdkidl/IWMProfile::RemoveStream
ms.prod: windows
ms.technology: windows-sdk
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
 - qasf.dll
api_name:
 - IWMProfile.RemoveStream
 - IWMProfile2.RemoveStream
 - IWMProfile3.RemoveStream
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMProfile::RemoveStream


## -description



The <b>RemoveStream</b> method removes a stream from the profile.




## -parameters




### -param pConfig [in]

Pointer to the <a href="https://msdn.microsoft.com/e013996a-95b6-4cd3-9fb5-75dbce821eef">IWMStreamConfig</a> interface of the stream configuration object that describes the stream you want to remove.


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



<a href="https://msdn.microsoft.com/34e30edb-3247-4eaa-9a63-6d94c9e37c0b">IWMProfile2</a>



<a href="https://msdn.microsoft.com/7942aa81-ada7-4e9c-a261-f257f8f890b7">IWMProfile3</a>



<a href="https://msdn.microsoft.com/3024fd2b-c261-49bd-b9a7-c1f43b31645b">IWMProfile::AddStream</a>



<a href="https://msdn.microsoft.com/72ecc794-d393-416e-bc21-5a7756e76d99">IWMProfile::RemoveStreamByNumber</a>
 

 

