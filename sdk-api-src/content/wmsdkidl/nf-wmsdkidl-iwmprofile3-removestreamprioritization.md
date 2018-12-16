---
UID: NF:wmsdkidl.IWMProfile3.RemoveStreamPrioritization
title: IWMProfile3::RemoveStreamPrioritization
author: windows-sdk-content
description: The RemoveStreamPrioritization method removes the stream prioritization object from the profile.
old-location: wmformat\iwmprofile3_removestreamprioritization.htm
tech.root: wmformat
ms.assetid: 1522cb9f-ce3f-4183-8779-3ee112efb40b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMProfile3 interface [windows Media Format],RemoveStreamPrioritization method, IWMProfile3.RemoveStreamPrioritization, IWMProfile3::RemoveStreamPrioritization, IWMProfile3RemoveStreamPrioritization, RemoveStreamPrioritization, RemoveStreamPrioritization method [windows Media Format], RemoveStreamPrioritization method [windows Media Format],IWMProfile3 interface, wmformat.iwmprofile3_removestreamprioritization, wmsdkidl/IWMProfile3::RemoveStreamPrioritization
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
 - IWMProfile3.RemoveStreamPrioritization
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMProfile3::RemoveStreamPrioritization


## -description



The <b>RemoveStreamPrioritization</b> method removes the stream prioritization object from the profile.




## -parameters






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
<dt><b>ASF_E_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
No stream prioritization object exists in the profile.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd757268(v=VS.85).aspx">IWMProfile3 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757380(v=VS.85).aspx">IWMProfile3::GetStreamPrioritization</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757384(v=VS.85).aspx">IWMProfile3::SetStreamPrioritization</a>
 

 

