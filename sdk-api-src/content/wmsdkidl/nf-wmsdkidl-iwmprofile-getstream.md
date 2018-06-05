---
UID: NF:wmsdkidl.IWMProfile.GetStream
title: IWMProfile::GetStream
author: windows-sdk-content
description: The GetStream method retrieves a stream from the profile.
old-location: wmformat\iwmprofile_getstream.htm
old-project: wmformat
ms.assetid: 067c3f03-a79a-4693-b963-7081f79c72d3
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetStream, GetStream method [windows Media Format], GetStream method [windows Media Format],IWMProfile interface, GetStream method [windows Media Format],IWMProfile2 interface, GetStream method [windows Media Format],IWMProfile3 interface, IWMProfile interface [windows Media Format],GetStream method, IWMProfile.GetStream, IWMProfile2 interface [windows Media Format],GetStream method, IWMProfile2::GetStream, IWMProfile3 interface [windows Media Format],GetStream method, IWMProfile3::GetStream, IWMProfile::GetStream, IWMProfileGetStream, wmformat.iwmprofile_getstream, wmsdkidl/IWMProfile2::GetStream, wmsdkidl/IWMProfile3::GetStream, wmsdkidl/IWMProfile::GetStream
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
-	IWMProfile.GetStream
-	IWMProfile2.GetStream
-	IWMProfile3.GetStream
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMProfile::GetStream


## -description



The <b>GetStream</b> method retrieves a stream from the profile.




## -parameters




### -param dwStreamIndex [in]

<b>DWORD</b> containing the stream index.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppConfig</i> or <i>dwStreamIndex</i> parameter is not valid.

</td>
</tr>
</table>
 




## -remarks



You can use this method in conjunction with <a href="https://msdn.microsoft.com/49534bc3-9115-422b-b448-b6f9c6ec1c47">GetStreamCount</a> to step through all of the streams in the profile.




## -see-also




<a href="https://msdn.microsoft.com/00f28d6b-d27d-4268-960e-c8ea25e5359e">IWMProfile Interface</a>



<a href="https://msdn.microsoft.com/34e30edb-3247-4eaa-9a63-6d94c9e37c0b">IWMProfile2</a>



<a href="https://msdn.microsoft.com/7942aa81-ada7-4e9c-a261-f257f8f890b7">IWMProfile3</a>



<a href="https://msdn.microsoft.com/507b1c55-1ecb-41dd-a6e5-298e1047a7ea">IWMProfile::GetStreamByNumber</a>
 

 

