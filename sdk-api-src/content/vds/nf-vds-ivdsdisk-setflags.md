---
UID: NF:vds.IVdsDisk.SetFlags
title: IVdsDisk::SetFlags (vds.h)
description: Sets the flags of a disk object.
helpviewer_keywords: ["IVdsDisk interface [VDS]","SetFlags method","IVdsDisk.SetFlags","IVdsDisk::SetFlags","SetFlags","SetFlags method [VDS]","SetFlags method [VDS]","IVdsDisk interface","base.ivdsdisk_setflags","vds/IVdsDisk::SetFlags"]
old-location: base\ivdsdisk_setflags.htm
tech.root: base
ms.assetid: 0ede6a22-b15c-4afd-8d49-c963ea7e2052
ms.date: 12/05/2018
ms.keywords: IVdsDisk interface [VDS],SetFlags method, IVdsDisk.SetFlags, IVdsDisk::SetFlags, SetFlags, SetFlags method [VDS], SetFlags method [VDS],IVdsDisk interface, base.ivdsdisk_setflags, vds/IVdsDisk::SetFlags
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
 - IVdsDisk::SetFlags
 - vds/IVdsDisk::SetFlags
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
 - IVdsDisk.SetFlags
---

# IVdsDisk::SetFlags


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Sets the flags of a disk object.

## -parameters

### -param ulFlags [in]

A bitmask of <a href="/windows/desktop/api/vds/ne-vds-vds_disk_flag">VDS_DISK_FLAG</a> enumeration values specifying the flags to be set. Only the <b>VDS_DF_READ_ONLY</b> flag can be set using this method. All other flags are set or cleared by the VDS service.

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
The flag was set successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_DISK_NOT_INITIALIZED</b></dt>
<dt>0x80042417L</dt>
</dl>
</td>
<td width="60%">
The flag cannot be set on an uninitialized disk.

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
The method is not supported. Neither the basic provider nor the current dynamic provider support this method.

</td>
</tr>
</table>

## -remarks

VDS implements this method.

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsdisk">IVdsDisk</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsdisk3-getproperties2">IVdsDisk3::GetProperties2</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsdisk-clearflags">IVdsDisk::ClearFlags</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsdisk-getproperties">IVdsDisk::GetProperties</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_disk_flag">VDS_DISK_FLAG</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_disk_prop">VDS_DISK_PROP</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_disk_prop2">VDS_DISK_PROP2</a>