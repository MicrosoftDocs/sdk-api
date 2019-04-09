---
UID: NF:wmsdkidl.IWMMutualExclusion2.SetName
title: IWMMutualExclusion2::SetName (wmsdkidl.h)
author: windows-sdk-content
description: The SetName method assigns a name to a mutual exclusion object.
old-location: wmformat\iwmmutualexclusion2_setname.htm
tech.root: wmformat
ms.assetid: b288c28c-04bd-49a4-bf11-21d4968772d4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMMutualExclusion2 interface [windows Media Format],SetName method, IWMMutualExclusion2.SetName, IWMMutualExclusion2::SetName, IWMMutualExclusion2SetName, SetName, SetName method [windows Media Format], SetName method [windows Media Format],IWMMutualExclusion2 interface, wmformat.iwmmutualexclusion2_setname, wmsdkidl/IWMMutualExclusion2::SetName
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
 - IWMMutualExclusion2.SetName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMMutualExclusion2::SetName


## -description



The <b>SetName</b> method assigns a name to a mutual exclusion object.




## -parameters




### -param pwszName [in]

Pointer to a wide-character null-terminated string containing the name you want to assign.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate memory to hold the name.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd757239(v=VS.85).aspx">IWMMutualExclusion2 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757242(v=VS.85).aspx">IWMMutualExclusion2::GetName</a>
 

 

