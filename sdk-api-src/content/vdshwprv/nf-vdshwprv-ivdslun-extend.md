---
UID: NF:vdshwprv.IVdsLun.Extend
title: IVdsLun::Extend (vdshwprv.h)
description: The IVdsLun::Extend (vdshwprv.h) method extends a LUN by a specified number of bytes.
helpviewer_keywords: ["Extend","Extend method [VDS]","Extend method [VDS]","IVdsLun interface","IVdsLun interface [VDS]","Extend method","IVdsLun.Extend","IVdsLun::Extend","base.ivdslun_extend","vds/IVdsLun::Extend","vdshwprv/IVdsLun::Extend"]
old-location: base\ivdslun_extend.htm
tech.root: base
ms.assetid: 65520b6a-206a-4b90-b8cc-b7964d0cf102
ms.date: 08/08/2022
ms.keywords: Extend, Extend method [VDS], Extend method [VDS],IVdsLun interface, IVdsLun interface [VDS],Extend method, IVdsLun.Extend, IVdsLun::Extend, base.ivdslun_extend, vds/IVdsLun::Extend, vdshwprv/IVdsLun::Extend
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
 - IVdsLun::Extend
 - vdshwprv/IVdsLun::Extend
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
 - IVdsLun.Extend
---

# IVdsLun::Extend


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Extends a LUN by a specified 
   number of bytes.

## -parameters

### -param ullNumberOfBytesToAdd [in]

The number of bytes by which to extend the LUN. The number of bytes is not required to be an even multiple 
      of the block or sector size of the drives. The provider can round the number of bytes up or down to meet 
      alignment requirements or other restrictions. In most cases, the provider rounds up, ensuring that, with rare 
      exceptions, the LUN is extended by at least the number of bytes requested.

### -param pDriveIdArray [in]

A pointer to an array of drive GUIDs. The provider uses these drives to extend the LUN. The drives are 
      used in the specified sequence; the provider uses all of the extents on one drive before moving on to the next 
      and stops when the LUN has been extended by the requested number of bytes. 
      

Alternatively, the caller can direct the provider to select the drives automatically by passing 
       <b>NULL</b> in this parameter and zero in the <i>lNumberOfDrives</i> 
       parameter. Note that passing <b>NULL</b> is valid only if the 
       <i>lNumberOfDrives</i> parameter is zero.

### -param lNumberOfDrives [in]

The number of drives specified in the <i>pDriveIdArray</i> parameter. If the caller 
      passes zero, the provider selects the drives.

### -param ppAsync [out]

The address of an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> interface pointer, 
      which VDS initializes on return. Callers must release the interface. Use this interface to cancel, wait for, or 
      query the status of the operation.

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
This return value signals a software or communication problem inside a provider that caches information 
        about the array. Use the 
        <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a> method 
        followed by the 
        <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> method to restore 
        the cache.

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
The LUN object is no longer present.

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
The LUN is in a failed state and is unable to perform the requested operation.

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
Can be returned from any method that takes a <b>VDS_OBJECT_ID</b> constant. This 
        return value indicates that the identifier does not refer to an existing object.

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
Not enough free drives are present in the subsystem to complete this operation.

</td>
</tr>
</table>

## -remarks

Callers can specify a list of drives for the provider to use for extending the LUN, or direct 
    the provider to select the drives automatically.

After the LUN is extended, the caller should use the <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_update_properties">IOCTL_DISK_UPDATE_PROPERTIES</a> control code to make the updated disk size visible on the computer to which the LUN is unmasked.

Implementers must return a pointer to the <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> 
     interface for this method, regardless of whether the call initiates an asynchronous operation.

If the <i>ullNumberOfBytesToAdd</i> parameter is greater than the number of bytes available 
     on the drives specified in the <i>pDriveIdArray</i> parameter, use the specified drives first 
     and then select from whatever other drives are available. If there are not enough such drives to extend the LUN 
     by the requested number of bytes, return an error and do not extend the LUN.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a>



<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdslun">IVdsLun</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-shrink">IVdsLun::Shrink</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-createlun">IVdsSubSystem::CreateLun</a>
