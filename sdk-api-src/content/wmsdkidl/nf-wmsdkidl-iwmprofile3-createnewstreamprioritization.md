---
UID: NF:wmsdkidl.IWMProfile3.CreateNewStreamPrioritization
title: IWMProfile3::CreateNewStreamPrioritization
author: windows-sdk-content
description: The CreateNewStreamPrioritization method creates a new stream prioritization object.
old-location: wmformat\iwmprofile3_createnewstreamprioritization.htm
tech.root: wmformat
ms.assetid: 801a66fa-b72d-4282-953e-216fb9a56cd7
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: CreateNewStreamPrioritization, CreateNewStreamPrioritization method [windows Media Format], CreateNewStreamPrioritization method [windows Media Format],IWMProfile3 interface, IWMProfile3 interface [windows Media Format],CreateNewStreamPrioritization method, IWMProfile3.CreateNewStreamPrioritization, IWMProfile3::CreateNewStreamPrioritization, IWMProfile3CreateNewStreamPrioritization, wmformat.iwmprofile3_createnewstreamprioritization, wmsdkidl/IWMProfile3::CreateNewStreamPrioritization
ms.prod: windows-hardware
ms.technology: windows-devices
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
api_name:
 - IWMProfile3.CreateNewStreamPrioritization
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMProfile3::CreateNewStreamPrioritization


## -description



The <b>CreateNewStreamPrioritization</b> method creates a new stream prioritization object. After you create a stream prioritization object, use the methods of the <a href="https://msdn.microsoft.com/ef8ae275-c36a-492c-b57c-d640044ede93">IWMStreamPrioritization</a> interface to configure it. The configured stream prioritization object can then be assigned to the profile with a call to <a href="https://msdn.microsoft.com/16dfb205-2a0b-4dc8-a8f2-8981534018f1">SetStreamPrioritization</a>.




## -parameters




### -param ppSP [out]

Pointer to receive the address of the <b>IWMStreamPrioritization</b> interface of the new object.


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
NULL was passed as <i>ppSP</i>.

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



A profile can only contain one stream prioritization. When you assign a new stream prioritization to a profile, the previous one will be lost.




## -see-also




<a href="https://msdn.microsoft.com/7942aa81-ada7-4e9c-a261-f257f8f890b7">IWMProfile3 Interface</a>



<a href="https://msdn.microsoft.com/cb0345ce-6847-435b-8cbb-f8b93856af9f">Stream Prioritization Object</a>
 

 

