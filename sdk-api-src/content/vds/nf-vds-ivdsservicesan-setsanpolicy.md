---
UID: NF:vds.IVdsServiceSAN.SetSANPolicy
title: IVdsServiceSAN::SetSANPolicy
author: windows-sdk-content
description: Sets the disk SAN policy for the operating system.
old-location: base\ivdsservicesan_setsanpolicy.htm
tech.root: VDS
ms.assetid: e5cb0b5e-d181-44a7-8416-e9f8fb575423
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IVdsServiceSAN interface,SetSANPolicy method, IVdsServiceSAN.SetSANPolicy, IVdsServiceSAN::SetSANPolicy, SetSANPolicy, SetSANPolicy method, SetSANPolicy method,IVdsServiceSAN interface, base.ivdsservicesan_setsanpolicy, vds/IVdsServiceSAN::SetSANPolicy
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsServiceSAN.SetSANPolicy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsServiceSAN::SetSANPolicy


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Sets the disk <a href="https://msdn.microsoft.com/2da99388-8ee6-4e6b-98dc-52f12290c4dc">SAN policy</a> for the operating system.


## -parameters




### -param SanPolicy [in]

A value from the <a href="https://msdn.microsoft.com/2da99388-8ee6-4e6b-98dc-52f12290c4dc">VDS_SAN_POLICY</a> enumeration that specifies the SAN policy.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="https://msdn.microsoft.com/en-us/library/ms680746(v=VS.85).aspx">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_SET_SAN_POLICY</b></dt>
</dl>
</td>
<td width="60%">
A driver error was reported when setting the SAN policy.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/675e9ea8-06b6-4832-9311-17361e4781d4">IVdsServiceSAN</a>



<a href="https://msdn.microsoft.com/59602d97-2fdf-4d1b-b158-e545619397e0">IVdsServiceSAN::GetSANPolicy</a>
 

 

