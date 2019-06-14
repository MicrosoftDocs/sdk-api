---
UID: NF:vds.IVdsAdvancedDisk.QueryPartitions
title: IVdsAdvancedDisk::QueryPartitions (vds.h)
author: windows-sdk-content
description: Returns the details of all partitions on the current disk.
old-location: base\ivdsadvanceddisk_querypartitions.htm
tech.root: VDS
ms.assetid: ca02c5f8-11cd-4bdf-a376-3b146eb2aa70
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVdsAdvancedDisk interface [VDS],QueryPartitions method, IVdsAdvancedDisk.QueryPartitions, IVdsAdvancedDisk::QueryPartitions, QueryPartitions, QueryPartitions method [VDS], QueryPartitions method [VDS],IVdsAdvancedDisk interface, base.ivdsadvanceddisk_querypartitions, vds/IVdsAdvancedDisk::QueryPartitions
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
 - IVdsAdvancedDisk.QueryPartitions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsAdvancedDisk::QueryPartitions


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the details of all partitions on the current disk.


## -parameters




### -param ppPartitionPropArray [out]

A pointer to the array of 
      <a href="https://docs.microsoft.com/windows/desktop/api/vds/ns-vds-_vds_partition_prop">VDS_PARTITION_PROP</a> structures passed in by the caller. Callers must free this array by using the 
      <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.


### -param plNumberOfPartitions [out]

A pointer to the number of elements in the array returned in the <i>ppPartitionPropArray</i> parameter.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://docs.microsoft.com/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

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
The query was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The disk contains no partitions.

</td>
</tr>
</table>
 




## -remarks



If the disk contains extended partitions, this method returns only the first extended partition, regardless of how many extended partitions are on the disk. 
    A disk contains one extended partition for each logical drive. For more information about logical drives, see <a href="https://docs.microsoft.com/windows/desktop/VDS/disk-object">Disk Object</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VDS/disk-object">Disk Object</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/nn-vds-ivdsadvanceddisk">IVdsAdvancedDisk</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/ns-vds-_vds_partition_prop">VDS_PARTITION_PROP</a>
 

 

