---
UID: NF:wmsdkidl.IWMProfile.CreateNewStream
title: IWMProfile::CreateNewStream
author: windows-sdk-content
description: The CreateNewStream method creates a stream configuration object. You can use a stream configuration object to define the characteristics of a media stream.
old-location: wmformat\iwmprofile_createnewstream.htm
tech.root: wmformat
ms.assetid: 4a1478ff-00fb-46e2-97a3-e00e9c1b819a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateNewStream, CreateNewStream method [windows Media Format], CreateNewStream method [windows Media Format],IWMProfile interface, CreateNewStream method [windows Media Format],IWMProfile2 interface, CreateNewStream method [windows Media Format],IWMProfile3 interface, IWMProfile interface [windows Media Format],CreateNewStream method, IWMProfile.CreateNewStream, IWMProfile2 interface [windows Media Format],CreateNewStream method, IWMProfile2::CreateNewStream, IWMProfile3 interface [windows Media Format],CreateNewStream method, IWMProfile3::CreateNewStream, IWMProfile::CreateNewStream, IWMProfileCreateNewStream, wmformat.iwmprofile_createnewstream, wmsdkidl/IWMProfile2::CreateNewStream, wmsdkidl/IWMProfile3::CreateNewStream, wmsdkidl/IWMProfile::CreateNewStream
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
 - IWMProfile.CreateNewStream
 - IWMProfile2.CreateNewStream
 - IWMProfile3.CreateNewStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMProfile::CreateNewStream


## -description



The <b>CreateNewStream</b> method creates a stream configuration object. You can use a stream configuration object to define the characteristics of a media stream.




## -parameters




### -param guidStreamType [in]

GUID object specifying the major media type for the stream to be created (for example, WMMEDIATYPE_Video). The supported major types are listed in <a href="https://msdn.microsoft.com/00dcbb20-09ed-44c5-992c-20f3d17ad47c">Media Types</a>.


### -param ppConfig [out]

Pointer to a pointer to the <a href="https://msdn.microsoft.com/e013996a-95b6-4cd3-9fb5-75dbce821eef">IWMStreamConfig</a> interface of the created stream configuration object.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough available memory.

</td>
</tr>
</table>
 




## -remarks



It is not possible to have a stream configuration object other than as an element of a profile. After the stream has been configured, this object must be added to the profile by using the <a href="https://msdn.microsoft.com/3024fd2b-c261-49bd-b9a7-c1f43b31645b">AddStream</a> method.

When <b>CreateNewStream</b> is called, a valid stream number is specified for the new stream. Stream numbers are in the range of 1 through 63.




## -see-also




<a href="https://msdn.microsoft.com/00f28d6b-d27d-4268-960e-c8ea25e5359e">IWMProfile Interface</a>



<a href="https://msdn.microsoft.com/34e30edb-3247-4eaa-9a63-6d94c9e37c0b">IWMProfile2</a>



<a href="https://msdn.microsoft.com/7942aa81-ada7-4e9c-a261-f257f8f890b7">IWMProfile3</a>



<a href="https://msdn.microsoft.com/228e334c-9d9b-4604-a225-73af7af3255f">Stream Configuration Object</a>
 

 

