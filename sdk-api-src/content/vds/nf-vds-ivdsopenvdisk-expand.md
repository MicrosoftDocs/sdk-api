---
UID: NF:vds.IVdsOpenVDisk.Expand
title: IVdsOpenVDisk::Expand (vds.h)
description: Increases the size of a virtual disk to the maximum size available on a fixed or expandable disk.
helpviewer_keywords: ["Expand","Expand method","Expand method","IVdsOpenVDisk interface","IVdsOpenVDisk interface","Expand method","IVdsOpenVDisk.Expand","IVdsOpenVDisk::Expand","base.ivdsopenvdisk_expand","vds/IVdsOpenVDisk::Expand"]
old-location: base\ivdsopenvdisk_expand.htm
tech.root: base
ms.assetid: 6ba166de-8045-4ccb-8771-fc4dd9438c1f
ms.date: 12/05/2018
ms.keywords: Expand, Expand method, Expand method,IVdsOpenVDisk interface, IVdsOpenVDisk interface,Expand method, IVdsOpenVDisk.Expand, IVdsOpenVDisk::Expand, base.ivdsopenvdisk_expand, vds/IVdsOpenVDisk::Expand
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
 - IVdsOpenVDisk::Expand
 - vds/IVdsOpenVDisk::Expand
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
 - IVdsOpenVDisk.Expand
---

# IVdsOpenVDisk::Expand


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Increases the size of a virtual disk to the maximum size available on a fixed or expandable disk.

## -parameters

### -param Flags [in]

An <b>EXPAND_VIRTUAL_DISK_FLAG</b> enumeration value that specifies how the virtual disk is to be expanded. Must be set to EXPAND_VIRTUAL_DISK_FLAG_NONE.

### -param NewSize [in]

The desired size in bytes of the expanded virtual disk.

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

A virtual disk can be expanded only if it is detached.

The virtual disk must have been opened with access to perform metadata operations. This corresponds to the <b>VIRTUAL_DISK_ACCESS_METAOPS</b> value of the <a href="/windows/win32/api/virtdisk/ne-virtdisk-virtual_disk_access_mask-r1">VIRTUAL_DISK_ACCESS_MASK</a> enumeration.

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsopenvdisk">IVdsOpenVDisk</a>

