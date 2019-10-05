---
UID: NF:vds.IVdsRemovable.QueryMedia
title: IVdsRemovable::QueryMedia (vds.h)
author: windows-sdk-content
description: Updates the disk properties in the cache. Call IVdsDisk::GetProperties to get updated details about the current media.
old-location: base\ivdsremovable_querymedia.htm
tech.root: VDS
ms.assetid: 6a56be84-ddf3-4c82-9465-4cb683e993f6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVdsRemovable interface [VDS],QueryMedia method, IVdsRemovable.QueryMedia, IVdsRemovable::QueryMedia, QueryMedia, QueryMedia method [VDS], QueryMedia method [VDS],IVdsRemovable interface, base.ivdsremovable_querymedia, vds/IVdsRemovable::QueryMedia
ms.topic: method
f1_keywords: 
 - "vds/IVdsRemovable.QueryMedia"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsRemovable::QueryMedia


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Updates the disk 
   properties in the cache. Call 
   <a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsdisk-getproperties">IVdsDisk::GetProperties</a> to get updated details
   about the current media.
  


## -parameters






## -returns



This method can return standard HRESULT values, such as E_OUTOFMEMORY, and <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://docs.microsoft.com/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

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




<a href="https://docs.microsoft.com/windows/desktop/api/vds/nn-vds-ivdsremovable">IVdsRemovable</a>
 

 

