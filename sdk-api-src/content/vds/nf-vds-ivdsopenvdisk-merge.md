---
UID: NF:vds.IVdsOpenVDisk.Merge
title: IVdsOpenVDisk::Merge (vds.h)
description: Merges a child virtual disk with its parents in the differencing chain.
helpviewer_keywords: ["IVdsOpenVDisk interface","Merge method","IVdsOpenVDisk.Merge","IVdsOpenVDisk::Merge","Merge","Merge method","Merge method","IVdsOpenVDisk interface","base.ivdsopenvdisk_merge","vds/IVdsOpenVDisk::Merge"]
old-location: base\ivdsopenvdisk_merge.htm
tech.root: base
ms.assetid: b513e904-a6ff-494e-9f63-b5158467b245
ms.date: 12/05/2018
ms.keywords: IVdsOpenVDisk interface,Merge method, IVdsOpenVDisk.Merge, IVdsOpenVDisk::Merge, Merge, Merge method, Merge method,IVdsOpenVDisk interface, base.ivdsopenvdisk_merge, vds/IVdsOpenVDisk::Merge
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
 - IVdsOpenVDisk::Merge
 - vds/IVdsOpenVDisk::Merge
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
 - IVdsOpenVDisk.Merge
---

# IVdsOpenVDisk::Merge


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Merges a child virtual disk with its parents in the differencing chain.

## -parameters

### -param Flags [in]

A <b>MERGE_VIRTUAL_DISK_FLAG</b> enumeration value that specifies how the virtual disk is to be merged. Must be set to MERGE_VIRTUAL_DISK_FLAG_NONE.

### -param MergeDepth [in]

The number of parent disks in the differencing chain to merge together. The disk must have been open with a ReadWriteDepth at least equal to this value.

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

A virtual disk can be merged only if it is detached.

This method moves all data blocks from the child disk to the parent. However, it will not delete the invalidated child disks at the end of the operation.

The virtual disk must have been opened with read/write access.

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsopenvdisk">IVdsOpenVDisk</a>