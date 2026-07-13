---
UID: NF:vds.IVdsVDisk.GetHostVolume
title: IVdsVDisk::GetHostVolume (vds.h)
description: Returns an interface pointer to the volume object for the volume where the virtual disk resides.
helpviewer_keywords: ["GetHostVolume","GetHostVolume method","GetHostVolume method","IVdsVDisk interface","IVdsVDisk interface","GetHostVolume method","IVdsVDisk.GetHostVolume","IVdsVDisk::GetHostVolume","base.ivdsvdisk_gethostvolume","vds/IVdsVDisk::GetHostVolume"]
old-location: base\ivdsvdisk_gethostvolume.htm
tech.root: base
ms.assetid: e8ab5d3a-775d-4c80-9c18-d25b5dd169e6
ms.date: 12/05/2018
ms.keywords: GetHostVolume, GetHostVolume method, GetHostVolume method,IVdsVDisk interface, IVdsVDisk interface,GetHostVolume method, IVdsVDisk.GetHostVolume, IVdsVDisk::GetHostVolume, base.ivdsvdisk_gethostvolume, vds/IVdsVDisk::GetHostVolume
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
 - IVdsVDisk::GetHostVolume
 - vds/IVdsVDisk::GetHostVolume
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
 - IVdsVDisk.GetHostVolume
---

# IVdsVDisk::GetHostVolume


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns an interface pointer to the volume object for the volume where the virtual disk resides.

## -parameters

### -param ppVolume [out]

A pointer to a variable that receives an <a href="/windows/desktop/api/vds/nn-vds-ivdsvolume">IVdsVolume</a> interface pointer for the volume. Callers must release the interface pointer when it is no longer needed by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

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