---
UID: NF:vds.IVdsRemovable.QueryMedia
title: IVdsRemovable::QueryMedia
author: windows-sdk-content
description: Updates the disk properties in the cache. Call IVdsDisk::GetProperties to get updated details about the current media.
old-location: base\ivdsremovable_querymedia.htm
tech.root: VDS
ms.assetid: 6a56be84-ddf3-4c82-9465-4cb683e993f6
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IVdsRemovable interface [VDS],QueryMedia method, IVdsRemovable.QueryMedia, IVdsRemovable::QueryMedia, QueryMedia, QueryMedia method [VDS], QueryMedia method [VDS],IVdsRemovable interface, base.ivdsremovable_querymedia, vds/IVdsRemovable::QueryMedia
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IVdsRemovable.QueryMedia
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- vds.h
: 
- IVdsRemovable.QueryMedia
: 
---

# IVdsRemovable::QueryMedia


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Updates the disk 
   properties in the cache. Call 
   <a href="https://msdn.microsoft.com/d2046a26-852d-46b2-b060-98b4a2a92387">IVdsDisk::GetProperties</a> to get updated details
   about the current media.
  


## -parameters






## -returns



This method can return standard HRESULT values, such as E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="_com_hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

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
The method completed successfully.

</td>
</tr>
</table>
 




## -remarks



VDS sends a notification when a disk or volume event modifies disk or volume properties.




## -see-also




<a href="https://msdn.microsoft.com/86dcd76a-0de0-42f4-9360-87cf7ca4ebf6">IVdsRemovable</a>
 

 

