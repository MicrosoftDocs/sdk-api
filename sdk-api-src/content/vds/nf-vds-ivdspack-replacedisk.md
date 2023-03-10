---
UID: NF:vds.IVdsPack.ReplaceDisk
title: IVdsPack::ReplaceDisk (vds.h)
description: Not supported.This method is reserved for future use. (IVdsPack.ReplaceDisk)
helpviewer_keywords: ["IVdsPack interface [VDS]","ReplaceDisk method","IVdsPack.ReplaceDisk","IVdsPack::ReplaceDisk","ReplaceDisk","ReplaceDisk method [VDS]","ReplaceDisk method [VDS]","IVdsPack interface","base.ivdspack_replacedisk","vds/IVdsPack::ReplaceDisk"]
old-location: base\ivdspack_replacedisk.htm
tech.root: base
ms.assetid: 4fc59ed0-ef54-4834-90d3-309d297543e6
ms.date: 12/05/2018
ms.keywords: IVdsPack interface [VDS],ReplaceDisk method, IVdsPack.ReplaceDisk, IVdsPack::ReplaceDisk, ReplaceDisk, ReplaceDisk method [VDS], ReplaceDisk method [VDS],IVdsPack interface, base.ivdspack_replacedisk, vds/IVdsPack::ReplaceDisk
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
 - IVdsPack::ReplaceDisk
 - vds/IVdsPack::ReplaceDisk
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
 - IVdsPack.ReplaceDisk
---

# IVdsPack::ReplaceDisk


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Not supported.

This method is reserved for future use.

## -parameters

### -param OldDiskId [in]

The GUID of the old disk.

### -param NewDiskId [in]

The GUID of the new disk.

### -param ppAsync [out]

The address of an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> interface pointer, 
      which VDS initializes on return. Callers must release the interface. Use this interface to cancel, wait for, or 
      query the status of the operation.

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
The disk replacement completed successfully.

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
This method is not supported in this release.

</td>
</tr>
</table>

## -remarks

Callers can use this method for media migration (replacing an old disk with a new disk) or when repairing a 
    fault-tolerant set with a missing or failed member—especially for those providers that do not implement hot sparing.

The new disk must be in the same pack as the old disk and cannot contain data; it can have the wrong 
    partitioning style. In the event of a successful replacement, the old disk retains the partitioning style but no 
    valid volumes.

Implementers must return a pointer to the <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> 
    interface for this method, regardless of whether the call initiates an asynchronous operation. If your provider 
    does not implement hot sparing, it must support the failed-member scenario: start synchronizing the exposed 
    fault-tolerant volume again after the caller invokes the 
    <b>ReplaceDisk</b> method.
