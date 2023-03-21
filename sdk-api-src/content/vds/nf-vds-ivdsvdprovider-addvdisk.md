---
UID: NF:vds.IVdsVdProvider.AddVDisk
title: IVdsVdProvider::AddVDisk (vds.h)
description: Creates a virtual disk object for an existing virtual disk file.
helpviewer_keywords: ["AddVDisk","AddVDisk method","AddVDisk method","IVdsVdProvider interface","IVdsVdProvider interface","AddVDisk method","IVdsVdProvider.AddVDisk","IVdsVdProvider::AddVDisk","base.ivdsvdprovider_addvdisk","vds/IVdsVdProvider::AddVDisk"]
old-location: base\ivdsvdprovider_addvdisk.htm
tech.root: base
ms.assetid: ef154bf3-ad30-4e6e-8292-af2037eced02
ms.date: 12/05/2018
ms.keywords: AddVDisk, AddVDisk method, AddVDisk method,IVdsVdProvider interface, IVdsVdProvider interface,AddVDisk method, IVdsVdProvider.AddVDisk, IVdsVdProvider::AddVDisk, base.ivdsvdprovider_addvdisk, vds/IVdsVdProvider::AddVDisk
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
 - IVdsVdProvider::AddVDisk
 - vds/IVdsVdProvider::AddVDisk
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
 - IVdsVdProvider.AddVDisk
---

# IVdsVdProvider::AddVDisk


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Creates a virtual disk object  for an existing virtual disk file.

## -parameters

### -param VirtualDeviceType [in]

The address of  a <a href="/windows/win32/api/virtdisk/ns-virtdisk-virtual_storage_type">VIRTUAL_STORAGE_TYPE</a> structure

### -param pPath [in]

A <b>NULL</b>-terminated wide-character string containing the name and directory path for the backing file for the virtual disk.

### -param ppVDisk [out]

A pointer to a variable that receives an <a href="/windows/desktop/api/vds/nn-vds-ivdsvdisk">IVdsVDisk</a> interface pointer to the newly created virtual disk object. Callers must release the interface pointer when it is no longer needed by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

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