---
UID: NF:vdshwprv.IVdsLun.Shrink
title: IVdsLun::Shrink (vdshwprv.h)
description: Shrinks a LUN by a specified number of bytes.helpviewer_keywords: ["IVdsLun interface [VDS]","Shrink method","IVdsLun.Shrink","IVdsLun::Shrink","Shrink","Shrink method [VDS]","Shrink method [VDS]","IVdsLun interface","base.ivdslun_shrink","vds/IVdsLun::Shrink","vdshwprv/IVdsLun::Shrink"]
old-location: base\ivdslun_shrink.htm
tech.root: VDS
ms.assetid: a02f7741-c17a-48f3-a823-292613aa287b
ms.date: 12/05/2018
ms.keywords: IVdsLun interface [VDS],Shrink method, IVdsLun.Shrink, IVdsLun::Shrink, Shrink, Shrink method [VDS], Shrink method [VDS],IVdsLun interface, base.ivdslun_shrink, vds/IVdsLun::Shrink, vdshwprv/IVdsLun::Shrink
f1_keywords:
- vdshwprv/IVdsLun.Shrink
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Uuid.lib
- Uuid.dll
api_name:
- IVdsLun.Shrink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsLun::Shrink


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Shrinks a LUN by a specified 
   number of bytes.


## -parameters




### -param ullNumberOfBytesToRemove [in]

The number of bytes by which to shrink the LUN. The number of bytes is not required to be an even multiple 
      of the block or sector size.


### -param ppAsync [out]

The address of an <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> interface pointer. 
      Callers must release the interface. Use this interface to cancel, wait for, or query the status of the operation.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://docs.microsoft.com/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

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
        about the array. Use the <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a> 
        method followed by the <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> 
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
</table>
 




## -remarks



Implementers must return a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> 
    interface for this method, regardless of whether the call initiates an asynchronous operation.

After the LUN is shrunk, the caller should use the <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_update_properties">IOCTL_DISK_UPDATE_PROPERTIES</a> control code to make the updated disk size visible on the computer to which the LUN is unmasked.

Implementers must remove the bytes from the end of the LUN.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdslun">IVdsLun</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-extend">IVdsLun::Extend</a>
 

 

