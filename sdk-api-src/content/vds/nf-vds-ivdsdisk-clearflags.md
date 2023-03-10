---
UID: NF:vds.IVdsDisk.ClearFlags
title: IVdsDisk::ClearFlags (vds.h)
description: Clears the flags of a disk object.
helpviewer_keywords: ["ClearFlags","ClearFlags method [VDS]","ClearFlags method [VDS]","IVdsDisk interface","IVdsDisk interface [VDS]","ClearFlags method","IVdsDisk.ClearFlags","IVdsDisk::ClearFlags","base.ivdsdisk_clearflags","vds/IVdsDisk::ClearFlags"]
old-location: base\ivdsdisk_clearflags.htm
tech.root: base
ms.assetid: 3ee43acd-6dcc-40de-9bb6-de7cfb605f15
ms.date: 12/05/2018
ms.keywords: ClearFlags, ClearFlags method [VDS], ClearFlags method [VDS],IVdsDisk interface, IVdsDisk interface [VDS],ClearFlags method, IVdsDisk.ClearFlags, IVdsDisk::ClearFlags, base.ivdsdisk_clearflags, vds/IVdsDisk::ClearFlags
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
 - IVdsDisk::ClearFlags
 - vds/IVdsDisk::ClearFlags
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
 - IVdsDisk.ClearFlags
---

# IVdsDisk::ClearFlags


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Clears the flags of a disk object.

## -parameters

### -param ulFlags [in]

A bitmask of <a href="/windows/desktop/api/vds/ne-vds-vds_disk_flag">VDS_DISK_FLAG</a> enumeration values specifying the flags to be cleared. Only the <b>VDS_DF_READ_ONLY</b> flag can be cleared using this method. All other flags are set or cleared by the VDS service.

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

<a href="/windows/desktop/api/vds/nn-vds-ivdsdisk">IVdsDisk</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsdisk3-getproperties2">IVdsDisk3::GetProperties2</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsdisk-getproperties">IVdsDisk::GetProperties</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsdisk-setflags">IVdsDisk::SetFlags</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_disk_flag">VDS_DISK_FLAG</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_disk_prop">VDS_DISK_PROP</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_disk_prop2">VDS_DISK_PROP2</a>