---
UID: NF:vds.IVdsService.QueryFileSystemTypes
title: IVdsService::QueryFileSystemTypes (vds.h)
description: Returns property details for all file systems known to VDS.
helpviewer_keywords: ["IVdsService interface [VDS]","QueryFileSystemTypes method","IVdsService.QueryFileSystemTypes","IVdsService::QueryFileSystemTypes","QueryFileSystemTypes","QueryFileSystemTypes method [VDS]","QueryFileSystemTypes method [VDS]","IVdsService interface","base.ivdsservice_queryfilesystemtypes","vds/IVdsService::QueryFileSystemTypes"]
old-location: base\ivdsservice_queryfilesystemtypes.htm
tech.root: base
ms.assetid: 17dcafc8-8faf-4dc2-af24-7e1ab257201e
ms.date: 12/05/2018
ms.keywords: IVdsService interface [VDS],QueryFileSystemTypes method, IVdsService.QueryFileSystemTypes, IVdsService::QueryFileSystemTypes, QueryFileSystemTypes, QueryFileSystemTypes method [VDS], QueryFileSystemTypes method [VDS],IVdsService interface, base.ivdsservice_queryfilesystemtypes, vds/IVdsService::QueryFileSystemTypes
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
 - IVdsService::QueryFileSystemTypes
 - vds/IVdsService::QueryFileSystemTypes
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
 - IVdsService.QueryFileSystemTypes
---

# IVdsService::QueryFileSystemTypes


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns property details for all file systems known to VDS.

## -parameters

### -param ppFileSystemTypeProps [out]

The address of a pointer to a buffer holding an array of 
      <a href="/windows/desktop/api/vds/ns-vds-vds_file_system_type_prop">VDS_FILE_SYSTEM_TYPE_PROP</a> structures. 
      Callers must free the memory for the array and for the <b>pwszIllegalLabelCharSet</b> string 
      by using the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

### -param plNumberOfFileSystems [out]

The total number of file systems.

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
<dt><b>VDS_E_INITIALIZED_FAILED</b></dt>
<dt>0x80042401L</dt>
</dl>
</td>
<td width="60%">
VDS failed to initialize. If an application calls this method before the service finishes initializing, 
        the method is blocked until the initialization completes. If the initialization fails, this error is 
        returned.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsservice">IVdsService</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_file_system_type_prop">VDS_FILE_SYSTEM_TYPE_PROP</a>