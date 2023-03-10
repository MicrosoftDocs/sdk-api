---
UID: NF:vds.IVdsSubSystem2.CreateLun2
title: IVdsSubSystem2::CreateLun2 (vds.h)
description: The IVdsSubSystem2::CreateLun2 method (vds.h) creates a LUN. Automagic hints are provided using a VDS_HINTS2 structure instead of a VDS_HINTS structure.
helpviewer_keywords: ["CreateLun2","CreateLun2 method","CreateLun2 method","IVdsSubSystem2 interface","IVdsSubSystem2 interface","CreateLun2 method","IVdsSubSystem2.CreateLun2","IVdsSubSystem2::CreateLun2","base.ivdssubsystem2_createlun2","vds/IVdsSubSystem2::CreateLun2","vdshwprv/IVdsSubSystem2::CreateLun2"]
old-location: base\ivdssubsystem2_createlun2.htm
tech.root: base
ms.assetid: 1fa046dd-fac9-4246-a90b-1837206b164c
ms.date: 08/05/2022
ms.keywords: CreateLun2, CreateLun2 method, CreateLun2 method,IVdsSubSystem2 interface, IVdsSubSystem2 interface,CreateLun2 method, IVdsSubSystem2.CreateLun2, IVdsSubSystem2::CreateLun2, base.ivdssubsystem2_createlun2, vds/IVdsSubSystem2::CreateLun2, vdshwprv/IVdsSubSystem2::CreateLun2
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
 - IVdsSubSystem2::CreateLun2
 - vds/IVdsSubSystem2::CreateLun2
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
 - IVdsSubSystem2.CreateLun2
---

# IVdsSubSystem2::CreateLun2


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Creates a LUN. This method is identical to the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-createlun">IVdsSubSystem::CreateLun</a> method, except that automagic hints are provided using a <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hints2">VDS_HINTS2</a> structure instead of a <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hints">VDS_HINTS</a> structure.

## -parameters

### -param type [in]

A <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_lun_type">VDS_LUN_TYPE</a> enumeration value that specifies the LUN type. The new 
      LUN can be an automagic type or a specific RAID type, but not both. If the caller specifies an automagic type, one or more automagic hints should be specified in the <i>pHints</i> parameter. 

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

### -param pDriveIdArray [in]

A pointer to an array that contains a <a href="/windows/desktop/VDS/vds-data-types">VDS_OBJECT_ID</a> for each of the drives to be used to create the LUN. By specifying a non-<b>NULL</b> value for this parameter, the caller is requesting that the provider use all of the drives, in the order provided, using all of the extents on one drive before moving on to the 
      next, and stopping when the LUN has reached the requested size. 
      

Alternatively, the caller can direct the provider to select the drives automatically by passing 
       <b>NULL</b> in this parameter and 0 in <i>lNumberOfDrives</i>. (Pass 
       <b>NULL</b> if and only if <i>lNumberOfDrives</i> is 0.)

If the <i>type</i> parameter specifies an automagic type, this parameter should be <b>NULL</b>.

### -param lNumberOfDrives [in]

The number of drives specified in <i>pDriveIdArray</i>. If the caller passes 0, the 
      provider selects the drives.
      

If the <i>type</i> parameter specifies an automagic type, this parameter should be 0.

After the LUN is created, the caller can determine which drives are in use by calling the 
       <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunplex-queryextents">IVdsLunPlex::QueryExtents</a> method.

### -param pwszUnmaskingList [in]

A list specifying the computers to be granted access the LUN. The list is a 
      semicolon-delimited, <b>NULL</b>-terminated, human-readable string. 

If the value is "*", all computers that have an HBA port attached to the storage subsystem are to be granted access to the LUN. If the value is "", no computers are to be granted access to the LUN.<div class="alert"><b>Note</b>  In practice, if the value is "*", most hardware providers only grant the ports and initiators on the local computer access to the LUN.</div>
<div> </div>


If "*" or "" is specified, no other value can be specified.

For Fibre Channel networks and serial attached SCSI (SAS) networks, each entry is a 64-bit World-Wide Name (WWN) of each port to which the LUN is unmasked, 
       formatted as a hexadecimal string (16 characters long), most significant byte first. For 
       example, a WWN address of 01:23:45:67:89:AB:CD:EF is represented as "0123456789ABCDEF". For more information, see the T10 specifications for <a href="https://t10.org/drafts.htm#FibreChannel">Fibre Channel</a> and <a href="https://t10.org/drafts.htm#SCSI3_SAS">SAS</a>.

For iSCSI networks, each entry is an iSCSI qualified name (IQN) of each initiator to which the LUN is unmasked. A LUN unmasked 
       to a particular initiator is considered to be associated with that initiator.

<div class="alert"><b>Note</b>  The unmasking list can contain the same WWN or IQN more than once. The caller is not expected to remove 
       duplicates from the list or to validate the format of the WWN or IQN.</div>
<div> </div>
After the LUN is created, the caller can determine the actual unmasking list by calling the 
       <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-getproperties">IVdsLun::GetProperties</a> method.

### -param pHints2 [in]

Pointer to a <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hints2">VDS_HINTS2</a> structure that specifies the hints to be used in creating the LUN. The provider is not required to apply the hints to the LUN. The hints specified in the <b>VDS_HINTS2</b> structure are only a request to the provider.

After the LUN is created, the caller can determine the hints that the provider applied by calling the 
      <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun2-queryhints2">IVdsLun2::QueryHints2</a>  method.

If the <i>type</i> parameter specifies a non-automagic type, this parameter should be <b>NULL</b>.

### -param ppAsync [out]

The address of an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> interface pointer, 
      which VDS initializes on return. Callers must release the interface. Use this interface to cancel, wait for, or 
      query the status of the operation.

If <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsasync-wait">IVdsAsync::Wait</a> is called on the returned interface pointer and a success HRESULT value is returned, 
      the interfaces returned in the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_async_output">VDS_ASYNC_OUTPUT</a> 
      structure must be released by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method on each interface pointer. However, if <b>Wait</b> returns a failure HRESULT value, or if the <i>pHrResult</i> parameter of <b>Wait</b> receives a failure HRESULT value, the interface pointers in the <b>VDS_ASYNC_OUTPUT</b> structure are <b>NULL</b> and do not need to be released. You can test for success or failure HRESULT values by using the <a href="/windows/desktop/api/winerror/nf-winerror-succeeded">SUCCEEDED</a> and <a href="/windows/desktop/api/winerror/nf-winerror-failed">FAILED</a> macros defined in Winerror.h.

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
<dt><b>VDS_E_PROVIDER_CACHE_CORRUPT</b></dt>
<dt>0x8004241FL</dt>
</dl>
</td>
<td width="60%">
There is a software or communication problem inside a provider that caches information 
        about the array. Use the 
        <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a> method
        followed by the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> 
        method to restore the cache.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_DELETED</b></dt>
<dt>0x8004240BL</dt>
</dl>
</td>
<td width="60%">
The subsystem object is no longer present.

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
The subsystem is in a failed state and is unable to perform the requested operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_ANOTHER_CALL_IN_PROGRESS</b></dt>
<dt>0x80042404L</dt>
</dl>
</td>
<td width="60%">
Another operation is in progress; this operation cannot proceed until the previous operation or 
        operations are complete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_NOT_FOUND</b></dt>
<dt>0x80042405L</dt>
</dl>
</td>
<td width="60%">
The identifier does not refer to an existing object. This value can be returned from any method that takes a <b>VDS_OBJECT_ID</b> constant.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_NOT_SUPPORTED</b></dt>
<dt>0x80042400L</dt>
</dl>
</td>
<td width="60%">
This operation or combination of parameters is not supported by this provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_NOT_ENOUGH_SPACE</b></dt>
<dt>0x8004240FL</dt>
</dl>
</td>
<td width="60%">
There is not enough usable space for this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_NOT_ENOUGH_DRIVE</b></dt>
<dt>0x80042410L</dt>
</dl>
</td>
<td width="60%">
Too few free drives are present in the subsystem to complete this operation.

</td>
</tr>
</table>

## -remarks

By choosing appropriate values for the <i>type</i> and <i>pHints2</i> parameters, the caller can specify the attributes of the LUN wholly, partially, or minimally. The provider can 
    automatically include unspecified attributes, based on the automagic hints specified in the 
    <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hints2">VDS_HINTS2</a> structure that the <i>pHints</i> parameter points to.

<b>Notes to implementers:  </b>The provider must return an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> interface pointer in the <i>ppAsync</i> parameter, even if the call to this method does not initiate an asynchronous operation.

The list of WWNs and IQNs in the <i>pwszUnmaskingList</i> parameter may contain duplicate names. It is the provider's responsibility to validate all names in the list and remove duplicates if necessary.

In response to the <b>CreateLun2</b> method and 
    before unmasking the new LUN to any host, the provider should fill the first and last megabytes with zeros, 
    leaving the LUN uninitialized.

There is a subtle difference between the <b>E_INVALIDARG</b> and 
    <b>VDS_E_NOT_SUPPORTED</b> return values. Providers are not expected to implement every feature that the VDS 
    API can present to a client. For example, the 
    <b>CreateLun2</b> method exposes the ability to 
    create many different types of LUNs (for example, simple, mirror, striped, and parity). However, providers are not required to support all 
    types of LUNs. If the caller specifies a value for the <i>type</i> parameter that is not a valid <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_lun_type">VDS_LUN_TYPE</a> enumeration value, the provider should return <b>E_INVALIDARG</b>. If the caller specifies a valid <i>type</i> value that the provider does not support, the provider should return VDS_E_NOT_SUPPORTED.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsasync-wait">IVdsAsync::Wait</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a>



<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdslun">IVdsLun</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun2-queryhints2">IVdsLun2::QueryHints2</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-getproperties">IVdsLun::GetProperties</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunplex-queryextents">IVdsLunPlex::QueryExtents</a>



<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdssubsystem2">IVdsSubSystem2</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-createlun">IVdsSubSystem::CreateLun</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-queryluns">IVdsSubSystem::QueryLuns</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_async_output">VDS_ASYNC_OUTPUT</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hints2">VDS_HINTS2</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_lun_type">VDS_LUN_TYPE</a>
