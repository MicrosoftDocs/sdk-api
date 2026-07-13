---
UID: NF:vdshwprv.IVdsHwProviderStoragePools.QueryStoragePools
title: IVdsHwProviderStoragePools::QueryStoragePools (vdshwprv.h)
description: The IVdsHwProviderStoragePools::QueryStoragePools (vdshwprv.h) method returns an IEnumVdsObject enumeration object containing a list of the storage pools managed by the hardware provider.
helpviewer_keywords: ["IVdsHwProviderStoragePools interface","QueryStoragePools method","IVdsHwProviderStoragePools.QueryStoragePools","IVdsHwProviderStoragePools::QueryStoragePools","QueryStoragePools","QueryStoragePools method","QueryStoragePools method","IVdsHwProviderStoragePools interface","base.ivdshwproviderstoragepools_querystoragepools","vds/IVdsHwProviderStoragePools::QueryStoragePools","vdshwprv/IVdsHwProviderStoragePools::QueryStoragePools"]
old-location: base\ivdshwproviderstoragepools_querystoragepools.htm
tech.root: base
ms.assetid: 308c9821-927d-4b90-854d-b050f3730c22
ms.date: 08/08/2022
ms.keywords: IVdsHwProviderStoragePools interface,QueryStoragePools method, IVdsHwProviderStoragePools.QueryStoragePools, IVdsHwProviderStoragePools::QueryStoragePools, QueryStoragePools, QueryStoragePools method, QueryStoragePools method,IVdsHwProviderStoragePools interface, base.ivdshwproviderstoragepools_querystoragepools, vds/IVdsHwProviderStoragePools::QueryStoragePools, vdshwprv/IVdsHwProviderStoragePools::QueryStoragePools
req.header: vdshwprv.h
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
 - IVdsHwProviderStoragePools::QueryStoragePools
 - vdshwprv/IVdsHwProviderStoragePools::QueryStoragePools
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
 - IVdsHwProviderStoragePools.QueryStoragePools
---

# IVdsHwProviderStoragePools::QueryStoragePools


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a> enumeration object containing a list of the <a href="/windows/desktop/VDS/storage-pool-object">storage pools</a> managed by the hardware provider.

## -parameters

### -param ulFlags [in]

A bitmask of one or more <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_storage_pool_type">VDS_STORAGE_POOL_TYPE</a> flags that specify the types of storage pools to be queried. One of the flags must be either VDS_SPT_CONCRETE or VDS_SPT_PRIMORDIAL. The default value of this parameter is zero. A value of zero means that all storage pools should be queried.

### -param ullRemainingFreeSpace [in]

The minimum amount of free space, in bytes, that each storage pool must contain. The default value for this parameter is zero. A value of zero means that the storage pools can contain any amount of free space.

### -param pPoolAttributes [in]

A pointer to a <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_pool_attributes">VDS_POOL_ATTRIBUTES</a> structure that specifies the attribute values that the returned storage pools must have. The default value for this parameter is <b>NULL</b>. A value of <b>NULL</b> means that the storage pools can have any attribute values.

### -param ppEnum [out]

The address of an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a> interface 
      pointer that can be used to enumerate the storage pools. For more information, see <a href="/windows/desktop/VDS/working-with-enumeration-objects">Working with Enumeration Objects</a>. Callers must release the interface and each of the storage pool  objects when they are no longer needed by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.
     This parameter is required and cannot be <b>NULL</b>.

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

## -remarks

If the hardware provider does not manage any storage pools, this method returns an empty enumeration object.

If a non-<b>NULL</b> value is specified in the <i>pPoolAttributes</i> parameter, this method returns only storage pools that satisfy all of the attributes that are specified in the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_pool_attributes">VDS_POOL_ATTRIBUTES</a> structure. If any  minimum and maximum attributes are specified, the storage pools that are returned must match these attributes exactly. The hint attributes are used as hints to further filter the storage pools that satisfy all the specified attributes. If a specified attribute does not apply to any of the storage pools, this method returns S_OK with an empty enumeration object.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdshwproviderstoragepools">IVdsHwProviderStoragePools</a>
