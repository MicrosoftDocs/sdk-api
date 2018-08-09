---
UID: NF:vdshwprv.IVdsSubSystem2.GetDrive2
title: IVdsSubSystem2::GetDrive2
author: windows-sdk-content
description: Returns the specified drive. This method is identical to the IVdsSubSystem::GetDrive method, except that it includes the enclosure number as a parameter.
old-location: base\ivdssubsystem2_getdrive2.htm
old-project: vds
ms.assetid: 5646da50-5ebd-44d8-b2e1-b3e96b9a6d3c
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetDrive2, GetDrive2 method, GetDrive2 method,IVdsSubSystem2 interface, IVdsSubSystem2 interface,GetDrive2 method, IVdsSubSystem2.GetDrive2, IVdsSubSystem2::GetDrive2, base.ivdssubsystem2_getdrive2, vds/IVdsSubSystem2::GetDrive2, vdshwprv/IVdsSubSystem2::GetDrive2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vdshwprv.h
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
tech.root: 
req.typenames: VDS_VERSION_SUPPORT_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsSubSystem2.GetDrive2
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsSubSystem2::GetDrive2


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns the specified drive. This method is identical to the <a href="https://msdn.microsoft.com/855e9991-606c-4fcc-ba1d-ebdb928d4c3e">IVdsSubSystem::GetDrive</a> method, except that it includes the enclosure number as a parameter.


## -parameters




### -param sBusNumber [in]

The number of the bus to which the drive is connected.


### -param sSlotNumber [in]

The number of the slot the drive occupies.


### -param ulEnclosureNumber [in]

The number of the enclosure that contains the drive. This parameter corresponds to the <b>ulEnclosureNumber</b> member of the <a href="https://msdn.microsoft.com/af932865-abb3-4dee-a7dc-3aa06fd167f6">VDS_DRIVE_PROP2</a> structure.


### -param ppDrive [out]

The address of an <a href="https://msdn.microsoft.com/597917cf-fb02-4949-98c3-3da3f7449ed1">IVdsDrive</a> interface pointer. Callers 
      must release the interface.


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
<dt><b>VDS_E_PROVIDER_CACHE_CORRUPT</b></dt>
<dt>0x8004241FL</dt>
</dl>
</td>
<td width="60%">
There is a software or communication problem inside a provider that caches information about 
        the array. Use the <a href="https://msdn.microsoft.com/aeb06a98-8896-446f-abd5-ea40be0bea40">IVdsHwProvider::Reenumerate</a> 
        method followed by the  <a href="https://msdn.microsoft.com/25ddc73c-5d1b-4bec-bbc2-9f22a5f82ffe">IVdsHwProvider::Refresh</a> 
        method to restore the cache.
       

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
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_STATUS_FAILED</b></dt>
<dt>0x80042431L</dt>
</dl>
</td>
<td width="60%">
The subsystem is in a failed state and is unable to perform the requested operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_ANOTHER_CALL_IN_PROGRESS</b></dt>
<dt>0x80042404L</dt>
</dl>
</td>
<td width="60%">
Another operation is in progress; this operation cannot proceed until the previous operation or operations 
        are complete.
       

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6d8115e3-2a47-4bc3-9a69-24e26f555f41">IVdsDrive2</a>



<a href="https://msdn.microsoft.com/aeb06a98-8896-446f-abd5-ea40be0bea40">IVdsHwProvider::Reenumerate</a>



<a href="https://msdn.microsoft.com/25ddc73c-5d1b-4bec-bbc2-9f22a5f82ffe">IVdsHwProvider::Refresh</a>



<a href="https://msdn.microsoft.com/7d19792c-cd37-4ea7-8830-c33c489e63e6">IVdsSubSystem2</a>



<a href="https://msdn.microsoft.com/855e9991-606c-4fcc-ba1d-ebdb928d4c3e">IVdsSubSystem::GetDrive</a>



<a href="https://msdn.microsoft.com/7d54922f-0531-4eab-afa9-f51ce6c75bfe">IVdsSubSystem::QueryDrives</a>
 

 

