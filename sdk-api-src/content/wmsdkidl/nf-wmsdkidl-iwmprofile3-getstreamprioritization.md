---
UID: NF:wmsdkidl.IWMProfile3.GetStreamPrioritization
title: IWMProfile3::GetStreamPrioritization method
author: windows-driver-content
description: The GetStreamPrioritization method retrieves the stream prioritization that exists in the profile.
old-location: wmformat\iwmprofile3_getstreamprioritization.htm
old-project: wmformat
ms.assetid: 09545c1e-8090-4526-9faf-6cb2cb369208
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: GetStreamPrioritization method [windows Media Format], GetStreamPrioritization method [windows Media Format], IWMProfile3 interface, GetStreamPrioritization,IWMProfile3.GetStreamPrioritization, IWMProfile3, IWMProfile3 interface [windows Media Format], GetStreamPrioritization method, IWMProfile3::GetStreamPrioritization, IWMProfile3GetStreamPrioritization, wmformat.iwmprofile3_getstreamprioritization, wmsdkidl/IWMProfile3::GetStreamPrioritization
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
api_name:
-	IWMProfile3.GetStreamPrioritization
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMProfile3::GetStreamPrioritization method


## -description



The <b>GetStreamPrioritization</b> method retrieves the stream prioritization that exists in the profile.




## -parameters




### -param ppSP [out]

Pointer to receive the address of the <a href="https://msdn.microsoft.com/ef8ae275-c36a-492c-b57c-d640044ede93">IWMStreamPrioritization</a> interface of the stream prioritization object in the profile.


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
<i>ppSP</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method is unable to allocate memory for the stream prioritization object

</td>
</tr>
</table>
 




## -remarks



Many profiles do not have a stream prioritization assigned to them. If you call <b>GetStreamPrioritization</b> on such a profile, no error is returned, but the retrieved address is <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/7942aa81-ada7-4e9c-a261-f257f8f890b7">IWMProfile3 Interface</a>



<a href="https://msdn.microsoft.com/1522cb9f-ce3f-4183-8779-3ee112efb40b">IWMProfile3::RemoveStreamPrioritization</a>



<a href="https://msdn.microsoft.com/16dfb205-2a0b-4dc8-a8f2-8981534018f1">IWMProfile3::SetStreamPrioritization</a>



<a href="https://msdn.microsoft.com/ef8ae275-c36a-492c-b57c-d640044ede93">IWMStreamPrioritization Interface</a>



<a href="https://msdn.microsoft.com/cb0345ce-6847-435b-8cbb-f8b93856af9f">Stream Prioritization Object</a>
 

 

