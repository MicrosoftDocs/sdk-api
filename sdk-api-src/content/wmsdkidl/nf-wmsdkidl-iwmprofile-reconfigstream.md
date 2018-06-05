---
UID: NF:wmsdkidl.IWMProfile.ReconfigStream
title: IWMProfile::ReconfigStream
author: windows-sdk-content
description: The ReconfigStream method enables changes made to a stream configuration to be included in the profile. Use this method when you have made changes to a stream that has already been included in the profile.
old-location: wmformat\iwmprofile_reconfigstream.htm
old-project: wmformat
ms.assetid: ac6de14b-b754-4f61-9f9a-656885641fbc
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWMProfile interface [windows Media Format],ReconfigStream method, IWMProfile.ReconfigStream, IWMProfile2 interface [windows Media Format],ReconfigStream method, IWMProfile2::ReconfigStream, IWMProfile3 interface [windows Media Format],ReconfigStream method, IWMProfile3::ReconfigStream, IWMProfile::ReconfigStream, IWMProfileReconfigStream, ReconfigStream, ReconfigStream method [windows Media Format], ReconfigStream method [windows Media Format],IWMProfile interface, ReconfigStream method [windows Media Format],IWMProfile2 interface, ReconfigStream method [windows Media Format],IWMProfile3 interface, wmformat.iwmprofile_reconfigstream, wmsdkidl/IWMProfile2::ReconfigStream, wmsdkidl/IWMProfile3::ReconfigStream, wmsdkidl/IWMProfile::ReconfigStream
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
-	IWMProfile.ReconfigStream
-	IWMProfile2.ReconfigStream
-	IWMProfile3.ReconfigStream
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMProfile::ReconfigStream


## -description



The <b>ReconfigStream</b> method enables changes made to a stream configuration to be included in the profile. Use this method when you have made changes to a stream that has already been included in the profile.




## -parameters




### -param pConfig [in]

Pointer to the <a href="https://msdn.microsoft.com/e013996a-95b6-4cd3-9fb5-75dbce821eef">IWMStreamConfig</a> interface of the stream configuration object for the stream you want to reconfigure.


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



You can call either <a href="https://msdn.microsoft.com/067c3f03-a79a-4693-b963-7081f79c72d3">IWMProfile::GetStream</a> or <a href="https://msdn.microsoft.com/507b1c55-1ecb-41dd-a6e5-298e1047a7ea">IWMProfile::GetStreamByNumber</a> to retrieve a stream already added to a profile.

If you create a new stream by calling <a href="https://msdn.microsoft.com/4a1478ff-00fb-46e2-97a3-e00e9c1b819a">IWMProfile::CreateNewStream</a>, you must call <a href="https://msdn.microsoft.com/3024fd2b-c261-49bd-b9a7-c1f43b31645b">IWMProfile::AddStream</a> to include it in the profile. Calling <b>ReconfigStream</b> on a new stream will result in an error.

Updating a stream configuration object has no effect on the profile until the application calls <b>ReconfigStream</b>.




## -see-also




<a href="https://msdn.microsoft.com/00f28d6b-d27d-4268-960e-c8ea25e5359e">IWMProfile Interface</a>



<a href="https://msdn.microsoft.com/34e30edb-3247-4eaa-9a63-6d94c9e37c0b">IWMProfile2</a>



<a href="https://msdn.microsoft.com/7942aa81-ada7-4e9c-a261-f257f8f890b7">IWMProfile3</a>
 

 

