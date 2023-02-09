---
UID: NF:vds.IVdsVolumeMF2.GetFileSystemTypeName
title: IVdsVolumeMF2::GetFileSystemTypeName (vds.h)
description: Retrieves the name of the file system on a volume.
helpviewer_keywords: ["GetFileSystemTypeName","GetFileSystemTypeName method","GetFileSystemTypeName method","IVdsVolumeMF2 interface","IVdsVolumeMF2 interface","GetFileSystemTypeName method","IVdsVolumeMF2.GetFileSystemTypeName","IVdsVolumeMF2::GetFileSystemTypeName","base.ivdsvolumemf2_getfilesystemtypename","vds/IVdsVolumeMF2::GetFileSystemTypeName"]
old-location: base\ivdsvolumemf2_getfilesystemtypename.htm
tech.root: base
ms.assetid: f9e8627b-0531-4dcb-9818-7560372aa4b0
ms.date: 12/05/2018
ms.keywords: GetFileSystemTypeName, GetFileSystemTypeName method, GetFileSystemTypeName method,IVdsVolumeMF2 interface, IVdsVolumeMF2 interface,GetFileSystemTypeName method, IVdsVolumeMF2.GetFileSystemTypeName, IVdsVolumeMF2::GetFileSystemTypeName, base.ivdsvolumemf2_getfilesystemtypename, vds/IVdsVolumeMF2::GetFileSystemTypeName
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
 - IVdsVolumeMF2::GetFileSystemTypeName
 - vds/IVdsVolumeMF2::GetFileSystemTypeName
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
 - IVdsVolumeMF2.GetFileSystemTypeName
---

# IVdsVolumeMF2::GetFileSystemTypeName


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Retrieves the name of the file system on a volume.

## -parameters

### -param ppwszFileSystemTypeName [out]

Pointer that upon successful completion receives a null-terminated Unicode string with the file system name.

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

<a href="/windows/desktop/api/vds/nn-vds-ivdsvolumemf2">IVdsVolumeMF2</a>