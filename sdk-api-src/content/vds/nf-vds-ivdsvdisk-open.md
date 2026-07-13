---
UID: NF:vds.IVdsVDisk.Open
title: IVdsVDisk::Open (vds.h)
description: Opens a handle to the specified virtual disk file and returns an IVdsOpenVDisk interface pointer to the object that represents the opened handle.
helpviewer_keywords: ["IVdsVDisk interface","Open method","IVdsVDisk.Open","IVdsVDisk::Open","Open","Open method","Open method","IVdsVDisk interface","base.ivdsvdisk_open","vds/IVdsVDisk::Open"]
old-location: base\ivdsvdisk_open.htm
tech.root: base
ms.assetid: e633f934-8f2d-4614-b34c-87bb74ebf385
ms.date: 12/05/2018
ms.keywords: IVdsVDisk interface,Open method, IVdsVDisk.Open, IVdsVDisk::Open, Open, Open method, Open method,IVdsVDisk interface, base.ivdsvdisk_open, vds/IVdsVDisk::Open
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
 - IVdsVDisk::Open
 - vds/IVdsVDisk::Open
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
 - IVdsVDisk.Open
---

# IVdsVDisk::Open


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Opens a handle to the specified virtual disk file and returns an <a href="/windows/desktop/api/vds/nn-vds-ivdsopenvdisk">IVdsOpenVDisk</a> interface pointer to the object that represents the opened handle.

## -parameters

### -param AccessMask [in]

A bitmask of <a href="/windows/win32/api/virtdisk/ne-virtdisk-virtual_disk_access_mask-r1">VIRTUAL_DISK_ACCESS_MASK</a> flags specifying the access rights to be applied to the opened virtual disk.

### -param Flags [in]

A bitmask of <a href="/windows/win32/api/virtdisk/ne-virtdisk-open_virtual_disk_flag">OPEN_VIRTUAL_DISK_FLAG</a> flags specifying how the virtual disk is to be opened.

### -param ReadWriteDepth [in]

The number of stores (backing files), beginning with the child, of the backing store chain to open read/write. The remaining stores in the differencing chain will be opened read-only. (This is necessary for merge operations to succeed.)

### -param ppOpenVDisk [out]

A pointer to a variable that receives an <a href="/windows/desktop/api/vds/nn-vds-ivdsopenvdisk">IVdsOpenVDisk</a> interface pointer to the newly created object that represents the handle opened to the virtual disk object. Callers must release the interface pointer when it is no longer needed by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

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

## -remarks

Applications must initialize process-wide security by calling the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a> function. The <i>dwImpLevel</i> parameter should be set to <b>RPC_C_IMP_LEVEL_IMPERSONATE</b>.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>These actions are not required until Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsvdisk">IVdsVDisk</a>

