---
UID: NF:vdshwprv.IVdsLun.QueryActiveControllers
title: IVdsLun::QueryActiveControllers (vdshwprv.h)
description: The IVdsLun::QueryActiveControllers (vdshwprv.h) method returns an enumeration of currently active controllers.
helpviewer_keywords: ["IVdsLun interface [VDS]","QueryActiveControllers method","IVdsLun.QueryActiveControllers","IVdsLun::QueryActiveControllers","QueryActiveControllers","QueryActiveControllers method [VDS]","QueryActiveControllers method [VDS]","IVdsLun interface","base.ivdslun_queryactivecontrollers","vds/IVdsLun::QueryActiveControllers","vdshwprv/IVdsLun::QueryActiveControllers"]
old-location: base\ivdslun_queryactivecontrollers.htm
tech.root: base
ms.assetid: 82561e4a-f2c2-46da-96bb-fbd50d4f7c39
ms.date: 08/08/2022
ms.keywords: IVdsLun interface [VDS],QueryActiveControllers method, IVdsLun.QueryActiveControllers, IVdsLun::QueryActiveControllers, QueryActiveControllers, QueryActiveControllers method [VDS], QueryActiveControllers method [VDS],IVdsLun interface, base.ivdslun_queryactivecontrollers, vds/IVdsLun::QueryActiveControllers, vdshwprv/IVdsLun::QueryActiveControllers
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
 - IVdsLun::QueryActiveControllers
 - vdshwprv/IVdsLun::QueryActiveControllers
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
 - IVdsLun.QueryActiveControllers
---

# IVdsLun::QueryActiveControllers


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns an enumeration of currently active controllers—the controllers through which the LUN 
   is accessible.

## -parameters

### -param ppEnum [out]

The address of an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a> interface 
      pointer that can be used to enumerate the controllers in the subsystem as <a href="/windows/desktop/VDS/controller-object">controller objects</a>. For more information, see <a href="/windows/desktop/VDS/working-with-enumeration-objects">Working with Enumeration Objects</a>. Callers must release the interface and each of the controller objects when they are no longer needed by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

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
Returns the enumeration of active controllers. If the LUN has no active controllers, the enumeration is 
        empty.

</td>
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
</table>

## -remarks

Use the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-associatecontrollers">IVdsLun::AssociateControllers</a> 
    method to set the controller. Use the 
    <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontroller-queryassociatedluns">IVdsController::QueryAssociatedLuns</a> 
    method to query the LUNs associated with a particular controller.

Most subsystems offer only one active controller for a LUN, leaving the other controllers in standby mode. 
    However, some subsystem manufacturers do permit multiple simultaneously active controllers.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a>



<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdslun">IVdsLun</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-associatecontrollers">IVdsLun::AssociateControllers</a>
