---
UID: NF:vds.IVdsAsync.Cancel
title: IVdsAsync::Cancel (vds.h)
description: The IVdsAsync::Cancel (vds.h) method cancels the asynchronous operation.
helpviewer_keywords: ["Cancel","Cancel method [VDS]","Cancel method [VDS]","IVdsAsync interface","IVdsAsync interface [VDS]","Cancel method","IVdsAsync.Cancel","IVdsAsync::Cancel","base.ivdsasync_cancel","vds/IVdsAsync::Cancel","vdshwprv/IVdsAsync::Cancel"]
old-location: base\ivdsasync_cancel.htm
tech.root: base
ms.assetid: 40940cb8-46b7-4483-9952-ab053c49dad7
ms.date: 08/05/2022
ms.keywords: Cancel, Cancel method [VDS], Cancel method [VDS],IVdsAsync interface, IVdsAsync interface [VDS],Cancel method, IVdsAsync.Cancel, IVdsAsync::Cancel, base.ivdsasync_cancel, vds/IVdsAsync::Cancel, vdshwprv/IVdsAsync::Cancel
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
 - IVdsAsync::Cancel
 - vds/IVdsAsync::Cancel
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
 - IVdsAsync.Cancel
---

# IVdsAsync::Cancel


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Cancels the asynchronous 
   operation.



## -returns

This method can return standard HRESULT values, such as E_OUTOFMEMORY, and <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_NOT_SUPPORTED</b></dt>
<dt>0x80042400L</dt>
</dl>
</td>
<td width="60%">
The method is not supported. Neither the basic provider nor the current dynamic provider support this 
        method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OPERATION_CANCELED</b></dt>
<dt>0x8004240DL</dt>
</dl>
</td>
<td width="60%">
The operation has already been canceled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_CANCEL_TOO_LATE</b></dt>
<dt>0x8004240CL</dt>
</dl>
</td>
<td width="60%">
The operation has progressed too far to cancel.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INCOMPATIBLE_FILE_SYSTEM</b></dt>
<dt>0x80042425L</dt>
</dl>
</td>
<td width="60%">
The file system is incompatible with the specified operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INCOMPATIBLE_MEDIA</b></dt>
<dt>0x80042426L</dt>
</dl>
</td>
<td width="60%">
The media is incompatible with this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_ACCESS_DENIED</b></dt>
<dt>0x80042427L</dt>
</dl>
</td>
<td width="60%">
Access is denied. An application using VDS must run under the Backup Operator or Administrators group 
        account.

</td>
</tr>
</table>

## -remarks

Dynamic providers do not implement this method. The basic provider checks for this method only when cleaning 
    a disk and does not implement it for any other operation.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a>
