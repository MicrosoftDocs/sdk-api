---
UID: NF:vds.IVdsVolumeMF.GetFileSystemProperties
title: IVdsVolumeMF::GetFileSystemProperties (vds.h)
description: Returns property details about the file system on the current volume.
helpviewer_keywords: ["GetFileSystemProperties","GetFileSystemProperties method [VDS]","GetFileSystemProperties method [VDS]","IVdsVolumeMF interface","IVdsVolumeMF interface [VDS]","GetFileSystemProperties method","IVdsVolumeMF.GetFileSystemProperties","IVdsVolumeMF::GetFileSystemProperties","base.ivdsvolumemf_getfilesystemproperties","vds/IVdsVolumeMF::GetFileSystemProperties"]
old-location: base\ivdsvolumemf_getfilesystemproperties.htm
tech.root: base
ms.assetid: 43f5495c-5a60-44fd-b217-16464c4693a4
ms.date: 12/05/2018
ms.keywords: GetFileSystemProperties, GetFileSystemProperties method [VDS], GetFileSystemProperties method [VDS],IVdsVolumeMF interface, IVdsVolumeMF interface [VDS],GetFileSystemProperties method, IVdsVolumeMF.GetFileSystemProperties, IVdsVolumeMF::GetFileSystemProperties, base.ivdsvolumemf_getfilesystemproperties, vds/IVdsVolumeMF::GetFileSystemProperties
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
 - IVdsVolumeMF::GetFileSystemProperties
 - vds/IVdsVolumeMF::GetFileSystemProperties
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
 - IVdsVolumeMF.GetFileSystemProperties
---

# IVdsVolumeMF::GetFileSystemProperties


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns property details about the file system on the current volume.

## -parameters

### -param pFileSystemProp [out]

The address of the <a href="/windows/desktop/api/vds/ns-vds-vds_file_system_prop">VDS_FILE_SYSTEM_PROP</a> 
      structure allocated and passed in by the caller. VDS allocates memory for the 
      <b>pwszLabel</b> member string. Callers must free the string by using the 
      <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_VOLUME_NOT_MOUNTED</b></dt>
<dt>0x8004244FL</dt>
</dl>
</td>
<td width="60%">
The volume has been taken offline.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_STATUS_FAILED</b></dt>
<dt>0x80042431L</dt>
</dl>
</td>
<td width="60%">
The volume failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PACK_OFFLINE</b></dt>
<dt>0x80042444L</dt>
</dl>
</td>
<td width="60%">
The pack containing the volume is not accessible.

</td>
</tr>
</table>

## -remarks

If the volume is encrypted by BitLocker, the type member of the <a href="/windows/desktop/api/vds/ns-vds-vds_file_system_prop">VDS_FILE_SYSTEM_PROP</a> structure will be set to <b>VDS_FST_UNKNOWN</b> on return.

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsvolumemf">IVdsVolumeMF</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_file_system_prop">VDS_FILE_SYSTEM_PROP</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_file_system_type">VDS_FILE_SYSTEM_TYPE</a>