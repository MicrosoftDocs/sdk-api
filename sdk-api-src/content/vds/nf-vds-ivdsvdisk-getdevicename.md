---
UID: NF:vds.IVdsVDisk.GetDeviceName
title: IVdsVDisk::GetDeviceName (vds.h)
description: Returns the device name for the volume where the virtual disk resides.
helpviewer_keywords: ["GetDeviceName","GetDeviceName method","GetDeviceName method","IVdsVDisk interface","IVdsVDisk interface","GetDeviceName method","IVdsVDisk.GetDeviceName","IVdsVDisk::GetDeviceName","base.ivdsvdisk_getdevicename","vds/IVdsVDisk::GetDeviceName"]
old-location: base\ivdsvdisk_getdevicename.htm
tech.root: base
ms.assetid: 4ce60f7f-a7f2-4e1e-aae0-bd082b62480f
ms.date: 12/05/2018
ms.keywords: GetDeviceName, GetDeviceName method, GetDeviceName method,IVdsVDisk interface, IVdsVDisk interface,GetDeviceName method, IVdsVDisk.GetDeviceName, IVdsVDisk::GetDeviceName, base.ivdsvdisk_getdevicename, vds/IVdsVDisk::GetDeviceName
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsVDisk::GetDeviceName
 - vds/IVdsVDisk::GetDeviceName
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
 - IVdsVDisk.GetDeviceName
---

# IVdsVDisk::GetDeviceName


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the device name for the volume where the virtual disk resides.

## -parameters

### -param ppDeviceName [out]

A pointer to a variable that receives a string that contains the device name for the volume.

## -returns

This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

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

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsvdisk">IVdsVDisk</a>