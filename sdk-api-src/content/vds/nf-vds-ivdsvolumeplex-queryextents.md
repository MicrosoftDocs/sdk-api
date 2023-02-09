---
UID: NF:vds.IVdsVolumePlex.QueryExtents
title: IVdsVolumePlex::QueryExtents (vds.h)
description: Returns all extents for the current plex.
helpviewer_keywords: ["IVdsVolumePlex interface [VDS]","QueryExtents method","IVdsVolumePlex.QueryExtents","IVdsVolumePlex::QueryExtents","QueryExtents","QueryExtents method [VDS]","QueryExtents method [VDS]","IVdsVolumePlex interface","base.ivdsvolumeplex_queryextents","vds/IVdsVolumePlex::QueryExtents"]
old-location: base\ivdsvolumeplex_queryextents.htm
tech.root: base
ms.assetid: 09548bcc-29b9-498f-a4c0-99428f26343a
ms.date: 12/05/2018
ms.keywords: IVdsVolumePlex interface [VDS],QueryExtents method, IVdsVolumePlex.QueryExtents, IVdsVolumePlex::QueryExtents, QueryExtents, QueryExtents method [VDS], QueryExtents method [VDS],IVdsVolumePlex interface, base.ivdsvolumeplex_queryextents, vds/IVdsVolumePlex::QueryExtents
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
 - IVdsVolumePlex::QueryExtents
 - vds/IVdsVolumePlex::QueryExtents
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
 - IVdsVolumePlex.QueryExtents
---

# IVdsVolumePlex::QueryExtents


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns all 
   extents for the current plex.

## -parameters

### -param ppExtentArray [out]

A pointer to the array of <a href="/windows/desktop/api/vds/ns-vds-vds_disk_extent">VDS_DISK_EXTENT</a> structures passed in by the caller. Callers must free this array by using the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

### -param plNumberOfExtents [out]

A pointer to a buffer containing the number of extents.

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

<a href="/windows/desktop/api/vds/nn-vds-ivdsvolumeplex">IVdsVolumePlex</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_disk_extent">VDS_DISK_EXTENT</a>