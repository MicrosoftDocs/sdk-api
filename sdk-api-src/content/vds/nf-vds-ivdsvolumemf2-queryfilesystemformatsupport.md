---
UID: NF:vds.IVdsVolumeMF2.QueryFileSystemFormatSupport
title: IVdsVolumeMF2::QueryFileSystemFormatSupport (vds.h)
description: Retrieves the properties of the file systems that are supported for formatting a volume.
helpviewer_keywords: ["IVdsVolumeMF2 interface","QueryFileSystemFormatSupport method","IVdsVolumeMF2.QueryFileSystemFormatSupport","IVdsVolumeMF2::QueryFileSystemFormatSupport","QueryFileSystemFormatSupport","QueryFileSystemFormatSupport method","QueryFileSystemFormatSupport method","IVdsVolumeMF2 interface","base.ivdsvolumemf2_queryfilesystemformatsupport","vds/IVdsVolumeMF2::QueryFileSystemFormatSupport"]
old-location: base\ivdsvolumemf2_queryfilesystemformatsupport.htm
tech.root: base
ms.assetid: 770a92fb-9e70-4db0-a782-b9064daef4ef
ms.date: 12/05/2018
ms.keywords: IVdsVolumeMF2 interface,QueryFileSystemFormatSupport method, IVdsVolumeMF2.QueryFileSystemFormatSupport, IVdsVolumeMF2::QueryFileSystemFormatSupport, QueryFileSystemFormatSupport, QueryFileSystemFormatSupport method, QueryFileSystemFormatSupport method,IVdsVolumeMF2 interface, base.ivdsvolumemf2_queryfilesystemformatsupport, vds/IVdsVolumeMF2::QueryFileSystemFormatSupport
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
 - IVdsVolumeMF2::QueryFileSystemFormatSupport
 - vds/IVdsVolumeMF2::QueryFileSystemFormatSupport
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
 - IVdsVolumeMF2.QueryFileSystemFormatSupport
---

# IVdsVolumeMF2::QueryFileSystemFormatSupport


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Retrieves the properties of the file systems that are supported for formatting a volume.

## -parameters

### -param ppFileSystemSupportProps [out]

A pointer to the array of <a href="/windows/desktop/api/vds/ns-vds-vds_file_system_format_support_prop">VDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP</a> structures passed in by the caller. Upon successful completion, these structures contain information about the properties of the supported file systems. Callers must free this array by using the 
      <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

### -param plNumberOfFileSystems [out]

A pointer to a variable that upon successful completion receives the total number of elements in array pointed to by the <i>ppFileSystemSupportProps</i> parameter.

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