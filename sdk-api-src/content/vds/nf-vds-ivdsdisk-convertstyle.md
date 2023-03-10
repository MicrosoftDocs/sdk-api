---
UID: NF:vds.IVdsDisk.ConvertStyle
title: IVdsDisk::ConvertStyle (vds.h)
description: Converts the partition style of an empty disk from one style to another.
helpviewer_keywords: ["ConvertStyle","ConvertStyle method [VDS]","ConvertStyle method [VDS]","IVdsDisk interface","IVdsDisk interface [VDS]","ConvertStyle method","IVdsDisk.ConvertStyle","IVdsDisk::ConvertStyle","base.ivdsdisk_convertstyle","vds/IVdsDisk::ConvertStyle"]
old-location: base\ivdsdisk_convertstyle.htm
tech.root: base
ms.assetid: 38c129cd-8e60-4e4a-b22b-26c69c68fe89
ms.date: 12/05/2018
ms.keywords: ConvertStyle, ConvertStyle method [VDS], ConvertStyle method [VDS],IVdsDisk interface, IVdsDisk interface [VDS],ConvertStyle method, IVdsDisk.ConvertStyle, IVdsDisk::ConvertStyle, base.ivdsdisk_convertstyle, vds/IVdsDisk::ConvertStyle
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsDisk::ConvertStyle
 - vds/IVdsDisk::ConvertStyle
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
 - IVdsDisk.ConvertStyle
---

# IVdsDisk::ConvertStyle


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Converts the partition style of an empty disk from one style to another.

## -parameters

### -param NewStyle [in]

The partition styles enumerated by <a href="/windows/desktop/api/vds/ne-vds-vds_partition_style">VDS_PARTITION_STYLE</a>.

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
The conversion completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INVALID_OPERATION</b></dt>
<dt>0x80042415L</dt>
</dl>
</td>
<td width="60%">
The disk style cannot be converted, as is the case for 1394 or USB disks and unallocated disks.

</td>
</tr>
</table>

## -remarks

An empty disk contains no user data, OEM partitions, ESP partitions, or unknown partitions. Only LDM metadata partitions and MSR partitions are valid on an empty disk.

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsdisk">IVdsDisk</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_partition_info_gpt">VDS_PARTITION_INFO_GPT</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_partition_info_mbr">VDS_PARTITION_INFO_MBR</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_partition_style">VDS_PARTITION_STYLE</a>