---
UID: NF:vdshwprv.IVdsHwProviderPrivate.QueryIfCreatedLun
title: IVdsHwProviderPrivate::QueryIfCreatedLun (vdshwprv.h)
description: Enables VDS to determine whether the hardware provider manages the specified LUN.
helpviewer_keywords: ["IVdsHwProviderPrivate interface [VDS]","QueryIfCreatedLun method","IVdsHwProviderPrivate.QueryIfCreatedLun","IVdsHwProviderPrivate::QueryIfCreatedLun","QueryIfCreatedLun","QueryIfCreatedLun method [VDS]","QueryIfCreatedLun method [VDS]","IVdsHwProviderPrivate interface","base.ivdshwproviderprivate_queryifcreatedlun","vdshwprv/IVdsHwProviderPrivate::QueryIfCreatedLun"]
old-location: base\ivdshwproviderprivate_queryifcreatedlun.htm
tech.root: base
ms.assetid: 06ba3486-9381-4898-b639-3d94b83be857
ms.date: 12/05/2018
ms.keywords: IVdsHwProviderPrivate interface [VDS],QueryIfCreatedLun method, IVdsHwProviderPrivate.QueryIfCreatedLun, IVdsHwProviderPrivate::QueryIfCreatedLun, QueryIfCreatedLun, QueryIfCreatedLun method [VDS], QueryIfCreatedLun method [VDS],IVdsHwProviderPrivate interface, base.ivdshwproviderprivate_queryifcreatedlun, vdshwprv/IVdsHwProviderPrivate::QueryIfCreatedLun
req.header: vdshwprv.h
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
 - IVdsHwProviderPrivate::QueryIfCreatedLun
 - vdshwprv/IVdsHwProviderPrivate::QueryIfCreatedLun
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
 - IVdsHwProviderPrivate.QueryIfCreatedLun
---

# IVdsHwProviderPrivate::QueryIfCreatedLun


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Enables VDS to determine whether the hardware provider manages the specified LUN.

## -parameters

### -param pwszDevicePath [in]

A pointer to the path to the LUN on the local computer; a zero-terminated, human-readable string.

### -param pVdsLunInformation [in]

A pointer to the identification data of the specified LUN. See the <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a> structure.

### -param pLunId [out]

A pointer to the returned LUN GUID. If the provider does not manage the LUN, set this parameter to GUID_NULL.

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
The provider owns the LUN; returns the GUID of the LUN.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The provider does not own the LUN.

</td>
</tr>
</table>

## -remarks

Only VDS calls this method.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdshwproviderprivate">IVdsHwProviderPrivate</a>



<a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a>