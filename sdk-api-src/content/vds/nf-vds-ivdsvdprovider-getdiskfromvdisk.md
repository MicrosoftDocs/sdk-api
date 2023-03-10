---
UID: NF:vds.IVdsVdProvider.GetDiskFromVDisk
title: IVdsVdProvider::GetDiskFromVDisk (vds.h)
description: Returns an IVdsDisk interface pointer for a virtual disk given an IVdsVDisk interface pointer.
helpviewer_keywords: ["GetDiskFromVDisk","GetDiskFromVDisk method","GetDiskFromVDisk method","IVdsVdProvider interface","IVdsVdProvider interface","GetDiskFromVDisk method","IVdsVdProvider.GetDiskFromVDisk","IVdsVdProvider::GetDiskFromVDisk","base.ivdsvdprovider_getdiskfromvdisk","vds/IVdsVdProvider::GetDiskFromVDisk"]
old-location: base\ivdsvdprovider_getdiskfromvdisk.htm
tech.root: base
ms.assetid: e0f1e7ef-fd72-48f5-895d-feabde4a3ded
ms.date: 12/05/2018
ms.keywords: GetDiskFromVDisk, GetDiskFromVDisk method, GetDiskFromVDisk method,IVdsVdProvider interface, IVdsVdProvider interface,GetDiskFromVDisk method, IVdsVdProvider.GetDiskFromVDisk, IVdsVdProvider::GetDiskFromVDisk, base.ivdsvdprovider_getdiskfromvdisk, vds/IVdsVdProvider::GetDiskFromVDisk
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
 - IVdsVdProvider::GetDiskFromVDisk
 - vds/IVdsVdProvider::GetDiskFromVDisk
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
 - IVdsVdProvider.GetDiskFromVDisk
---

# IVdsVdProvider::GetDiskFromVDisk


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns an <a href="/windows/desktop/api/vds/nn-vds-ivdsdisk">IVdsDisk</a> interface pointer for a virtual disk given an <a href="/windows/desktop/api/vds/nn-vds-ivdsvdisk">IVdsVDisk</a> interface pointer.

## -parameters

### -param pVDisk [in]

The <a href="/windows/desktop/api/vds/nn-vds-ivdsvdisk">IVdsVDisk</a> interface pointer for the virtual disk.

### -param ppDisk [out]

A pointer to a variable that receives an <a href="/windows/desktop/api/vds/nn-vds-ivdsdisk">IVdsDisk</a> interface pointer. Callers must release the interface pointer when it is no longer needed by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

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

<a href="/windows/desktop/api/vds/nn-vds-ivdsvdprovider">IVdsVdProvider</a>