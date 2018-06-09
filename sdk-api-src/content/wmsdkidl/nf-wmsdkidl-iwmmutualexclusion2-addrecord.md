---
UID: NF:wmsdkidl.IWMMutualExclusion2.AddRecord
title: IWMMutualExclusion2::AddRecord
author: windows-sdk-content
description: The AddRecord method adds a record to the mutual exclusion object.
old-location: wmformat\iwmmutualexclusion2_addrecord.htm
old-project: wmformat
ms.assetid: 58eaa4b2-65d3-44b1-8e3d-1aac01057d0f
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: AddRecord, AddRecord method [windows Media Format], AddRecord method [windows Media Format],IWMMutualExclusion2 interface, IWMMutualExclusion2 interface [windows Media Format],AddRecord method, IWMMutualExclusion2.AddRecord, IWMMutualExclusion2::AddRecord, IWMMutualExclusion2AddRecord, wmformat.iwmmutualexclusion2_addrecord, wmsdkidl/IWMMutualExclusion2::AddRecord
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
api_name:
 - IWMMutualExclusion2.AddRecord
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMMutualExclusion2::AddRecord


## -description



The <b>AddRecord</b> method adds a record to the mutual exclusion object. Records can hold groups of streams. You can add streams with calls to <a href="https://msdn.microsoft.com/501fae9f-84b3-4025-83bc-ad0bbe47384d">IWMMutualExclusion2::AddStreamForRecord</a>. You can assign a name to a record with a call to <a href="https://msdn.microsoft.com/b288c28c-04bd-49a4-bf11-21d4968772d4">IWMMutualExclusion2::SetName</a>.




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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate memory for the new record.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
There was a problem adding the new record to the collection of records for this mutual exclusion object.

</td>
</tr>
</table>
 




## -remarks



Record numbers, which are used by other methods, are assigned to records sequentially.




## -see-also




<a href="https://msdn.microsoft.com/4a1f468c-2ba5-48a1-b56f-8b62aacf1ccf">IWMMutualExclusion2 Interface</a>



<a href="https://msdn.microsoft.com/501fae9f-84b3-4025-83bc-ad0bbe47384d">IWMMutualExclusion2::AddStreamForRecord</a>



<a href="https://msdn.microsoft.com/74e2825e-2200-4750-bb16-f8cf9f80ab7e">IWMMutualExclusion2::RemoveRecord</a>



<a href="https://msdn.microsoft.com/b288c28c-04bd-49a4-bf11-21d4968772d4">IWMMutualExclusion2::SetName</a>
 

 

