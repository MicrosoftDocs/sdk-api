---
UID: NF:vds.IVdsDiskPartitionMF.QueryPartitionFileSystemFormatSupport
title: IVdsDiskPartitionMF::QueryPartitionFileSystemFormatSupport (vds.h)
description: Retrieves the properties of the file systems that are supported for formatting a partition on the disk at a specified byte offset.
helpviewer_keywords: ["IVdsDiskPartitionMF interface","QueryPartitionFileSystemFormatSupport method","IVdsDiskPartitionMF.QueryPartitionFileSystemFormatSupport","IVdsDiskPartitionMF::QueryPartitionFileSystemFormatSupport","QueryPartitionFileSystemFormatSupport","QueryPartitionFileSystemFormatSupport method","QueryPartitionFileSystemFormatSupport method","IVdsDiskPartitionMF interface","base.ivdsdiskpartitionmf_querypartitionfilesystemformatsupport","vds/IVdsDiskPartitionMF::QueryPartitionFileSystemFormatSupport"]
old-location: base\ivdsdiskpartitionmf_querypartitionfilesystemformatsupport.htm
tech.root: base
ms.assetid: 7ee61c81-28d2-43d8-8444-a62dc025aed0
ms.date: 12/05/2018
ms.keywords: IVdsDiskPartitionMF interface,QueryPartitionFileSystemFormatSupport method, IVdsDiskPartitionMF.QueryPartitionFileSystemFormatSupport, IVdsDiskPartitionMF::QueryPartitionFileSystemFormatSupport, QueryPartitionFileSystemFormatSupport, QueryPartitionFileSystemFormatSupport method, QueryPartitionFileSystemFormatSupport method,IVdsDiskPartitionMF interface, base.ivdsdiskpartitionmf_querypartitionfilesystemformatsupport, vds/IVdsDiskPartitionMF::QueryPartitionFileSystemFormatSupport
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsDiskPartitionMF::QueryPartitionFileSystemFormatSupport
 - vds/IVdsDiskPartitionMF::QueryPartitionFileSystemFormatSupport
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsDiskPartitionMF.QueryPartitionFileSystemFormatSupport
---

# IVdsDiskPartitionMF::QueryPartitionFileSystemFormatSupport


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Retrieves the properties of the file systems that are supported for formatting a partition on the disk at a specified byte offset.

## -parameters

### -param ullOffset [in]

Byte offset of the partition from the beginning of the disk.  This offset must be the offset of the start of a partition.

### -param ppFileSystemSupportProps [out]

A pointer to the array of <a href="/windows/desktop/api/vds/ns-vds-vds_file_system_format_support_prop">VDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP</a> structures passed in by the caller. Upon successful completion, this array receives information about the properties of the supported file systems. Callers must free this array by using the 
      <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

### -param plNumberOfFileSystems [out]

A pointer to a variable that upon successful completion receives the total number of elements in the <i>ppFileSystemSupportProps</i> parameter.

## -returns

This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_BAD_PROVIDER_DATA</b></dt>
<dt>0x80042441L</dt>
</dl>
</td>
<td width="60%">
A provider returned bad data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_DISK_REMOVEABLE</b></dt>
<dt>0x8004255AL</dt>
</dl>
</td>
<td width="60%">
The operation is not supported on removable media.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_MISSING_DISK</b></dt>
<dt>0x80042454L</dt>
</dl>
</td>
<td width="60%">
The disk is missing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_NOT_FOUND</b></dt>
<dt>0x80042405L</dt>
</dl>
</td>
<td width="60%">
The partition does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PARTITION_NOT_OEM</b></dt>
<dt>0x8004256FL</dt>
</dl>
</td>
<td width="60%">
The operation is not supported on non-OEM partitions.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsdiskpartitionmf">IVdsDiskPartitionMF</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_file_system_format_support_prop">VDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP</a>