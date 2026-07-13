---
UID: NF:vds.IVdsOpenVDisk.Compact
title: IVdsOpenVDisk::Compact (vds.h)
description: Compacts the virtual disk to reduce the physical size of the backing file.
helpviewer_keywords: ["Compact","Compact method","Compact method","IVdsOpenVDisk interface","IVdsOpenVDisk interface","Compact method","IVdsOpenVDisk.Compact","IVdsOpenVDisk::Compact","base.ivdsopenvdisk_compact","vds/IVdsOpenVDisk::Compact"]
old-location: base\ivdsopenvdisk_compact.htm
tech.root: base
ms.assetid: 011adaae-3a17-4643-ae8d-400753019c83
ms.date: 12/05/2018
ms.keywords: Compact, Compact method, Compact method,IVdsOpenVDisk interface, IVdsOpenVDisk interface,Compact method, IVdsOpenVDisk.Compact, IVdsOpenVDisk::Compact, base.ivdsopenvdisk_compact, vds/IVdsOpenVDisk::Compact
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
 - IVdsOpenVDisk::Compact
 - vds/IVdsOpenVDisk::Compact
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
 - IVdsOpenVDisk.Compact
---

# IVdsOpenVDisk::Compact


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Compacts the virtual disk to reduce the physical size of the backing file.

## -parameters

### -param Flags [in]

A <b>COMPACT_VIRTUAL_DISK_FLAG</b> enumeration value that specifies how the virtual disk is to be compacted. Must be set to COMPACT_VIRTUAL_DISK_FLAG_NONE.

### -param Reserved [in]

This parameter is reserved for system use.

### -param ppAsync [out]

A pointer to an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> interface that upon successful completion receives the <b>IVdsAsync</b> interface to monitor and control this operation.  Callers must release the interface received when they have finished with it.  If the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsasync-wait">IVdsAsync::Wait</a> method is called on the interface and a success HRESULT value is returned, the interfaces returned in the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_async_output">VDS_ASYNC_OUTPUT</a> structure must be released by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method on each interface pointer. However, if <b>Wait</b> returns a failure HRESULT value, or if the <i>pHrResult</i> parameter of <b>Wait</b> receives a failure HRESULT value, the interface pointers in the <b>VDS_ASYNC_OUTPUT</b> structure are <b>NULL</b> and do not need to be released. You can test for success or failure HRESULT values by using the <a href="/windows/desktop/api/winerror/nf-winerror-succeeded">SUCCEEDED</a> and <a href="/windows/desktop/api/winerror/nf-winerror-failed">FAILED</a> macros defined in Winerror.h.

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

A virtual disk can be compacted only if it is in one of the following states:

<ul>
<li>Detached (offline mode)</li>
<li>Attached and opened with read-only access (online mode)</li>
</ul>
If it is in any other state, the compact operation fails.

The virtual disk must be an expandable (also called dynamic) or differencing virtual disk.

The operation can be safely interrupted and re-run later. If the operation is interrupted and the backing file is reopened, the file's size may be reduced when the file is opened.

The operation can be CPU-intensive or I/O-intensive, or both, depending on how large the virtual disk is and how many unused blocks require manipulation.

This method reduces the size of the virtual disk's backing store file by reclaiming unused space. If this method is called for a virtual disk that is detached, it can only reclaim space in the file that was never used to write data. If it is called for a virtual disk that is attached and opened with read-only access, it is able to reclaim space that was once used, but was later freed. Calling this method for a virtual disk that is attached and opened with read-only access reclaims the maximum amount of free space in the backing store file.

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsopenvdisk">IVdsOpenVDisk</a>