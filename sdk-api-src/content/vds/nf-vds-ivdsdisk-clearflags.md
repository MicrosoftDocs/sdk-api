---
UID: NF:vds.IVdsDisk.ClearFlags
title: IVdsDisk::ClearFlags
author: windows-sdk-content
description: Clears the flags of a disk object.
old-location: base\ivdsdisk_clearflags.htm
old-project: VDS
ms.assetid: 3ee43acd-6dcc-40de-9bb6-de7cfb605f15
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ClearFlags, ClearFlags method [VDS], ClearFlags method [VDS],IVdsDisk interface, IVdsDisk interface [VDS],ClearFlags method, IVdsDisk.ClearFlags, IVdsDisk::ClearFlags, base.ivdsdisk_clearflags, vds/IVdsDisk::ClearFlags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: VDS_VOLUME_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsDisk.ClearFlags
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsDisk::ClearFlags


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Clears the flags of a disk object.


## -parameters




### -param ulFlags [in]

A bitmask of <a href="https://msdn.microsoft.com/a421a1c1-a82c-4e07-846c-10aa2082ab86">VDS_DISK_FLAG</a> enumeration values specifying the flags to be cleared. Only the <b>VDS_DF_READ_ONLY</b> flag can be cleared using this method. All other flags are set or cleared by the VDS service.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The flag was cleared successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_NOT_SUPPORTED</b></dt>
<dt>0x80042400L</dt>
</dl>
</td>
<td width="60%">
The flag is not supported. Neither the basic provider nor the dynamic provider support this flag.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0fd6d1d4-daa6-4be3-8749-be98cd7c0288">IVdsDisk</a>



<a href="https://msdn.microsoft.com/ef88b61b-9139-4767-b54f-46122650e922">IVdsDisk3::GetProperties2</a>



<a href="https://msdn.microsoft.com/d2046a26-852d-46b2-b060-98b4a2a92387">IVdsDisk::GetProperties</a>



<a href="https://msdn.microsoft.com/0ede6a22-b15c-4afd-8d49-c963ea7e2052">IVdsDisk::SetFlags</a>



<a href="https://msdn.microsoft.com/a421a1c1-a82c-4e07-846c-10aa2082ab86">VDS_DISK_FLAG</a>



<a href="https://msdn.microsoft.com/c7c09f95-9489-46fd-8b03-cabdee4521cf">VDS_DISK_PROP</a>



<a href="https://msdn.microsoft.com/f51c2937-4b70-44fb-b626-1df072e2622a">VDS_DISK_PROP2</a>
 

 

