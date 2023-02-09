---
UID: NF:vds.IVdsHwProviderStoragePools.CreateLunInStoragePool
title: IVdsHwProviderStoragePools::CreateLunInStoragePool (vds.h)
description: The IVdsHwProviderStoragePools::CreateLunInStoragePool method (vds.h) creates a LUN in a storage pool.
helpviewer_keywords: ["CreateLunInStoragePool","CreateLunInStoragePool method","CreateLunInStoragePool method","IVdsHwProviderStoragePools interface","IVdsHwProviderStoragePools interface","CreateLunInStoragePool method","IVdsHwProviderStoragePools.CreateLunInStoragePool","IVdsHwProviderStoragePools::CreateLunInStoragePool","base.ivdshwproviderstoragepools_createluninstoragepool","vds/IVdsHwProviderStoragePools::CreateLunInStoragePool","vdshwprv/IVdsHwProviderStoragePools::CreateLunInStoragePool"]
old-location: base\ivdshwproviderstoragepools_createluninstoragepool.htm
tech.root: base
ms.assetid: 17377671-1a30-4aeb-bc89-3c1e3823d3fe
ms.date: 08/05/2022
ms.keywords: CreateLunInStoragePool, CreateLunInStoragePool method, CreateLunInStoragePool method,IVdsHwProviderStoragePools interface, IVdsHwProviderStoragePools interface,CreateLunInStoragePool method, IVdsHwProviderStoragePools.CreateLunInStoragePool, IVdsHwProviderStoragePools::CreateLunInStoragePool, base.ivdshwproviderstoragepools_createluninstoragepool, vds/IVdsHwProviderStoragePools::CreateLunInStoragePool, vdshwprv/IVdsHwProviderStoragePools::CreateLunInStoragePool
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
 - IVdsHwProviderStoragePools::CreateLunInStoragePool
 - vds/IVdsHwProviderStoragePools::CreateLunInStoragePool
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
 - IVdsHwProviderStoragePools.CreateLunInStoragePool
---

# IVdsHwProviderStoragePools::CreateLunInStoragePool


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Creates a LUN in a <a href="/windows/desktop/VDS/storage-pool-object">storage pool</a>.

## -parameters

### -param type [in]

A <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_lun_type">VDS_LUN_TYPE</a> enumeration value that specifies the type of LUN to be created. The new 
      LUN can be an automagic type or a specific RAID type, but not both. If the caller specifies an automagic type, one or more automagic hints should be specified in the <i>pHints2</i> parameter. 

The interface pointer for the new 
      <a href="/windows/desktop/VDS/lun-object">LUN object</a> can be retrieved by calling the 
      <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsasync-wait">IVdsAsync::Wait</a> method on the interface pointer returned in the 
      <i>ppAsync</i> parameter. The 
      <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_async_output">VDS_ASYNC_OUTPUT</a> structure returned by <b>Wait</b>  contains the 
      LUN object interface pointer in the <b>cl.pLunUnk</b> member.

### -param ullSizeInBytes [in]

The size, in bytes, of the new LUN. The provider can round the size up or down to meet alignment 
      requirements or other restrictions. (In most cases, the provider rounds up, ensuring that, with rare 
      exceptions, the LUN is at least as large as requested.) 
      

After the LUN is created, the caller can determine the actual size of the LUN by calling the 
       <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-getproperties">IVdsLun::GetProperties</a> method.

### -param StoragePoolId [in]

A <a href="/windows/desktop/VDS/vds-data-types">VDS_OBJECT_ID</a> value that identifies the storage pool where the LUN is to be created. This parameter is required and cannot be GUID_NULL.

### -param pwszUnmaskingList [in]

A list specifying the computers to be granted access the LUN. The list is a 
      semicolon-delimited, <b>NULL</b>-terminated, human-readable string.

 If the value is "*", all computers that have an HBA port attached to the storage subsystem are to be granted access to the LUN. If the value is "", no computers are to be granted access to the LUN.<div class="alert"><b>Note</b>  In practice, if the value is "*", most hardware providers only grant the ports and initiators on the local computer access to the LUN.</div>
<div> </div>


If "*" or "" is specified, no other value can be specified.

For Fibre Channel networks and serial attached SCSI (SAS) networks, each entry is a 64-bit World-Wide Name (WWN) of each port to which the LUN is unmasked, 
       formatted as a hexadecimal string (16 characters long), most significant byte first. For 
       example, a WWN address of 01:23:45:67:89:AB:CD:EF is represented as "0123456789ABCDEF". For more information, see the T10 specifications for <a href="https://t10.org/drafts.htm#FibreChannel">Fibre Channel</a> and <a href="https://t10.org/drafts.htm#SCSI3_SAS">SAS</a>.

For iSCSI networks, each entry is an iSCSI-qualified name (IQN) of each initiator to which the LUN is unmasked. A LUN unmasked 
       to a particular initiator is considered to be associated with that initiator.

<div class="alert"><b>Note</b>  The unmasking list can contain the same WWN or IQN more than once. The caller is not expected to remove 
       duplicates from the list or to validate the format of the WWN or IQN.</div>
<div> </div>
After the LUN is created, the caller can determine the actual unmasking list by calling the 
       <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-getproperties">IVdsLun::GetProperties</a> method.

### -param pHints2 [in]

A pointer to a <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hints2">VDS_HINTS2</a> structure that specifies the hints to be used in creating the LUN. The provider is not required to apply the hints to the LUN. The hints specified in the <b>VDS_HINTS2</b> structure are only a request to the provider.

After the LUN is created, the caller can determine the hints that the provider applied by calling the 
      <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun2-queryhints2">IVdsLun2::QueryHints2</a> method.

If the <i>type</i> parameter specifies a non-automagic type, this parameter should be <b>NULL</b>.

### -param ppAsync [out]

A pointer to an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> interface that upon successful completion receives the <b>IVdsAsync</b> interface to monitor and control this operation.  Callers must release the interface received when they are done with it.  If the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsasync-wait">IVdsAsync::Wait</a> method is called on the interface and a success HRESULT value is returned, the interfaces returned in the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_async_output">VDS_ASYNC_OUTPUT</a> structure must be released by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method on each interface pointer. However, if <b>Wait</b> returns a failure HRESULT value, or if the <i>pHrResult</i> parameter of <b>Wait</b> receives a failure HRESULT value, the interface pointers in the <b>VDS_ASYNC_OUTPUT</b> structure are <b>NULL</b> and do not need to be released. You can test for success or failure HRESULT values by using the <a href="/windows/desktop/api/winerror/nf-winerror-succeeded">SUCCEEDED</a> and <a href="/windows/desktop/api/winerror/nf-winerror-failed">FAILED</a> macros defined in Winerror.h.

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

By choosing appropriate values for the <i>type</i> and <i>pHints2</i> parameters, the caller can specify the attributes of the LUN wholly, partially, or minimally. The provider can 
    automatically include unspecified attributes, based on the automagic hints specified in the 
    <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hints2">VDS_HINTS2</a> structure that the <i>pHints2</i> parameter points to.

<b>Notes to implementers:  </b>The provider must return an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> interface pointer in the <i>ppAsync</i> parameter, even if the call to this method does not initiate an asynchronous operation.

The list of WWNs and IQNs in the <i>pwszUnmaskingList</i> parameter may contain duplicate names. It is the provider's responsibility to validate all names in the list and remove duplicates if necessary.

In response to the <b>CreateLunInStoragePool</b> method and 
    before unmasking the new LUN to any host, the provider should fill the first and last megabytes with zeros, 
    leaving the LUN uninitialized.

There is a subtle difference between the <b>E_INVALIDARG</b> and 
    <b>VDS_E_NOT_SUPPORTED</b> return values. Providers are not expected to implement every feature that the VDS 
    API can present to a client. For example, the 
    <b>CreateLunInStoragePool</b> method exposes the ability to 
    create many different types of LUNs (for example, simple, mirror, striped, and parity). However, providers are not required to support all 
    types of LUNs. If the caller specifies a value for the <i>type</i> parameter that is not a valid <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_lun_type">VDS_LUN_TYPE</a> enumeration value, the provider should return <b>E_INVALIDARG</b>. If the caller specifies a valid <i>type</i> value that the provider does not support, the provider should return VDS_E_NOT_SUPPORTED.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdshwproviderstoragepools">IVdsHwProviderStoragePools</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun2-queryhints2">IVdsLun2::QueryHints2</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-getproperties">IVdsLun::GetProperties</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hints2">VDS_HINTS2</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_lun_type">VDS_LUN_TYPE</a>
