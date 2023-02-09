---
UID: NF:vds.IVdsPack.RemoveMissingDisk
title: IVdsPack::RemoveMissingDisk (vds.h)
description: Removes a disk that is missing from the pack. This method applies to software provider objects only.
helpviewer_keywords: ["IVdsPack interface [VDS]","RemoveMissingDisk method","IVdsPack.RemoveMissingDisk","IVdsPack::RemoveMissingDisk","RemoveMissingDisk","RemoveMissingDisk method [VDS]","RemoveMissingDisk method [VDS]","IVdsPack interface","base.ivdspack_removemissingdisk","vds/IVdsPack::RemoveMissingDisk"]
old-location: base\ivdspack_removemissingdisk.htm
tech.root: base
ms.assetid: f7bdd5b9-430b-49c8-8476-be15eb3948c6
ms.date: 12/05/2018
ms.keywords: IVdsPack interface [VDS],RemoveMissingDisk method, IVdsPack.RemoveMissingDisk, IVdsPack::RemoveMissingDisk, RemoveMissingDisk, RemoveMissingDisk method [VDS], RemoveMissingDisk method [VDS],IVdsPack interface, base.ivdspack_removemissingdisk, vds/IVdsPack::RemoveMissingDisk
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
 - IVdsPack::RemoveMissingDisk
 - vds/IVdsPack::RemoveMissingDisk
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
 - IVdsPack.RemoveMissingDisk
---

# IVdsPack::RemoveMissingDisk


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Removes 
   a disk that is missing from the pack. This method applies to software provider objects only.

## -parameters

### -param DiskId [in]

The VDS_OBJECT_ID of the missing disk.

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
All details of the disk were removed successfully.

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
<i>DiskId</i> is a basic disk.

</td>
</tr>
</table>

## -remarks

Use this method for dynamic disks only.

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdspack">IVdsPack</a>