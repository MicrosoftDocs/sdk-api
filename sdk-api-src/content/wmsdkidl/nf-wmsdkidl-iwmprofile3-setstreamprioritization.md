---
UID: NF:wmsdkidl.IWMProfile3.SetStreamPrioritization
title: IWMProfile3::SetStreamPrioritization
author: windows-sdk-content
description: The SetStreamPrioritization method assigns a stream prioritization object to the profile. A profile can contain only one stream prioritization object at a time.
old-location: wmformat\iwmprofile3_setstreamprioritization.htm
old-project: wmformat
ms.assetid: 16dfb205-2a0b-4dc8-a8f2-8981534018f1
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWMProfile3 interface [windows Media Format],SetStreamPrioritization method, IWMProfile3.SetStreamPrioritization, IWMProfile3::SetStreamPrioritization, IWMProfile3SetStreamPrioritization, SetStreamPrioritization, SetStreamPrioritization method [windows Media Format], SetStreamPrioritization method [windows Media Format],IWMProfile3 interface, wmformat.iwmprofile3_setstreamprioritization, wmsdkidl/IWMProfile3::SetStreamPrioritization
ms.prod: windows
ms.technology: windows-sdk
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
-	IWMProfile3.SetStreamPrioritization
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMProfile3::SetStreamPrioritization


## -description



The <b>SetStreamPrioritization</b> method assigns a stream prioritization object to the profile. A profile can contain only one stream prioritization object at a time.




## -parameters




### -param pSP [in]

Pointer to the <a href="https://msdn.microsoft.com/ef8ae275-c36a-492c-b57c-d640044ede93">IWMStreamPrioritization</a> interface of the stream prioritization object you want to assign to the profile.


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
<dt><b>E_INVALID_ARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pSP</i> is <b>NULL</b>.

OR

The method was unable to validate the stream prioritization object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate memory in the profile for the object.

</td>
</tr>
</table>
 




## -remarks



If there is already a stream prioritization object in the profile, it will be lost.




## -see-also




<a href="https://msdn.microsoft.com/7942aa81-ada7-4e9c-a261-f257f8f890b7">IWMProfile3 Interface</a>



<a href="https://msdn.microsoft.com/09545c1e-8090-4526-9faf-6cb2cb369208">IWMProfile3::GetStreamPrioritization</a>



<a href="https://msdn.microsoft.com/1522cb9f-ce3f-4183-8779-3ee112efb40b">IWMProfile3::RemoveStreamPrioritization</a>
 

 

