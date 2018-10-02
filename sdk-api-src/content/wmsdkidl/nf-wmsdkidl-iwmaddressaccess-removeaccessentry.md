---
UID: NF:wmsdkidl.IWMAddressAccess.RemoveAccessEntry
title: IWMAddressAccess::RemoveAccessEntry
author: windows-sdk-content
description: The RemoveAccessEntry method removes an access entry.
old-location: wmformat\iwmaddressaccess_removeaccessentry.htm
tech.root: wmformat
ms.assetid: f3f9d493-90b4-4b2a-ad18-baf2b09bc72e
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMAddressAccess interface [windows Media Format],RemoveAccessEntry method, IWMAddressAccess.RemoveAccessEntry, IWMAddressAccess::RemoveAccessEntry, IWMAddressAccessRemoveAccessEntry, RemoveAccessEntry, RemoveAccessEntry method [windows Media Format], RemoveAccessEntry method [windows Media Format],IWMAddressAccess interface, wmformat.iwmaddressaccess_removeaccessentry, wmsdkidl/IWMAddressAccess::RemoveAccessEntry
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
 - IWMAddressAccess.RemoveAccessEntry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMAddressAccess::RemoveAccessEntry


## -description



The <b>RemoveAccessEntry</b> method removes an access entry.




## -parameters




### -param aeType [in]

A member of the <a href="https://msdn.microsoft.com/514e6745-c521-41bd-81c2-b6c24cfb0192">WM_AETYPE</a> enumeration specifying the type of entry to remove (exclusion or inclusion).


### -param dwEntryNum [in]

Zero-based index of the access entry to remove. Use the <a href="https://msdn.microsoft.com/996d8a8a-887e-4e2f-b810-c57a4251f771">IWMAddressAccess::GetAccessEntryCount</a> method to get the number of entries.


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
NULL pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_INDEX</b></dt>
</dl>
</td>
<td width="60%">
Invalid index number.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7251c600-90a2-4903-b26a-643b4d10b0ce">IWMAddressAccess Interface</a>
 

 

