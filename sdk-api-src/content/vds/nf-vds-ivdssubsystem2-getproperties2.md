---
UID: NF:vds.IVdsSubSystem2.GetProperties2
title: IVdsSubSystem2::GetProperties2
author: windows-sdk-content
description: Returns the properties of a subsystem. This method is identical to the IVdsSubSystem::GetProperties method, except that it returns a VDS_SUB_SYSTEM_PROP2 structure instead of a VDS_SUB_SYSTEM_PROP structure.
old-location: base\ivdssubsystem2_getproperties2.htm
tech.root: VDS
ms.assetid: 1f2164a9-643d-4762-8a2e-31d5c277502e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetProperties2, GetProperties2 method, GetProperties2 method,IVdsSubSystem2 interface, IVdsSubSystem2 interface,GetProperties2 method, IVdsSubSystem2.GetProperties2, IVdsSubSystem2::GetProperties2, base.ivdssubsystem2_getproperties2, vds/IVdsSubSystem2::GetProperties2, vdshwprv/IVdsSubSystem2::GetProperties2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IVdsSubSystem2.GetProperties2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsSubSystem2::GetProperties2


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns the properties of a subsystem. This method is identical to the <a href="https://msdn.microsoft.com/cbcf1e14-7e3d-44e6-8c4a-afe927ed0f9d">IVdsSubSystem::GetProperties</a> method, except that it returns a <a href="https://msdn.microsoft.com/8eb743b5-26e6-42e5-b94b-0849b1280cdb">VDS_SUB_SYSTEM_PROP2</a> structure instead of a <a href="https://msdn.microsoft.com/8fecb874-5c59-4f55-b528-040ff9209612">VDS_SUB_SYSTEM_PROP</a> structure.


## -parameters




### -param pSubSystemProp2

TBD




#### - pSubSystemProp [out]

The address of the <a href="https://msdn.microsoft.com/8eb743b5-26e6-42e5-b94b-0849b1280cdb">VDS_SUB_SYSTEM_PROP2</a> 
      structure allocated and passed in by the caller. VDS allocates memory for the 
      <b>pwszFriendlyName</b> and <b>pwszIdentification</b> member strings. 
      Callers must free the strings by using the 
      <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="https://msdn.microsoft.com/en-us/library/ms680746(v=VS.85).aspx">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_S_PROPERTIES_INCOMPLETE</b></b></dt>
<dt>0x00042715L</dt>
</dl>
</td>
<td width="60%">
Some but not all of the properties were successfully retrieved. Note that there are many possible reasons for failing to retrieve all properties, including device removal.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PROVIDER_CACHE_CORRUPT</b></dt>
<dt>0x8004241FL</dt>
</dl>
</td>
<td width="60%">
There is a software or communication problem inside a provider that caches information 
        about the array. Use the 
        <a href="https://msdn.microsoft.com/aeb06a98-8896-446f-abd5-ea40be0bea40">IVdsHwProvider::Reenumerate</a> method 
        followed by the 
        <a href="https://msdn.microsoft.com/25ddc73c-5d1b-4bec-bbc2-9f22a5f82ffe">IVdsHwProvider::Refresh</a> method to restore 
        the cache.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_DELETED</b></dt>
<dt>0x8004240BL</dt>
</dl>
</td>
<td width="60%">
The subsystem object is no longer present.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7d19792c-cd37-4ea7-8830-c33c489e63e6">IVdsSubSystem2</a>
 

 

