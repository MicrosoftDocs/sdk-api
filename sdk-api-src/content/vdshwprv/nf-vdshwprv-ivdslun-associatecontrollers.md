---
UID: NF:vdshwprv.IVdsLun.AssociateControllers
title: IVdsLun::AssociateControllers (vdshwprv.h)
description: The IVdsLun::AssociateControllers (vdshwprv.h) method sets the subsystem controllers to active or inactive with respect to the LUN.
helpviewer_keywords: ["AssociateControllers","AssociateControllers method [VDS]","AssociateControllers method [VDS]","IVdsLun interface","IVdsLun interface [VDS]","AssociateControllers method","IVdsLun.AssociateControllers","IVdsLun::AssociateControllers","base.ivdslun_associatecontrollers","vds/IVdsLun::AssociateControllers","vdshwprv/IVdsLun::AssociateControllers"]
old-location: base\ivdslun_associatecontrollers.htm
tech.root: base
ms.assetid: 2c3dc668-1745-49f4-9cd1-3bf0b322d0b2
ms.date: 08/08/2022
ms.keywords: AssociateControllers, AssociateControllers method [VDS], AssociateControllers method [VDS],IVdsLun interface, IVdsLun interface [VDS],AssociateControllers method, IVdsLun.AssociateControllers, IVdsLun::AssociateControllers, base.ivdslun_associatecontrollers, vds/IVdsLun::AssociateControllers, vdshwprv/IVdsLun::AssociateControllers
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
 - IVdsLun::AssociateControllers
 - vdshwprv/IVdsLun::AssociateControllers
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
 - IVdsLun.AssociateControllers
---

# IVdsLun::AssociateControllers


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Sets the subsystem controllers to active or inactive with respect to the LUN.

## -parameters

### -param pActiveControllerIdArray [in]

A pointer to an array of controller GUIDs. The provider sets these controllers to active. This array 
      includes controllers already set to active that are to remain so.

### -param lNumberOfActiveControllers [in]

The number of controllers specified in the <i>pActiveControllerArray</i> parameter.

### -param pInactiveControllerIdArray [in]

A pointer to an array of controller GUIDs. The provider sets these controllers to inactive. This array 
      includes controllers already set to inactive that are to remain so.

### -param lNumberOfInactiveControllers [in]

The number of controllers specified in the  <i>pInactiveControllerIdArray</i> parameter.

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
Another operation is in progress. This operation cannot proceed until the previous operation or 
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
One or more of the GUIDs specified in the active or inactive arrays do not refer to an existing object.

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
</table>

## -remarks

The caller must include each subsystem controller in exactly one of either the 
    <i>pActiveControllerIdArray</i> parameter or the 
    <i>pInactiveControllerIdArray</i> parameter for each method call. The composition of the 
    <i>pActiveControllerIdArray</i> and <i>pInactiveControllerIdArray</i> 
    parameters can be different for each of the subsystem LUNs. Most subsystems implement only one active controller, 
    but some allow for multiple active controllers.

<div class="alert"><b>Note</b>  The <b>E_INVALIDARG</b> return value can indicate that the caller did not specify all 
     controllers in the subsystem.  The 
     <b>AssociateControllers</b> method requires 
     that all controllers in the subsystem be present in one of the two arrays supplied.</div>
<div> </div>
Use the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-queryactivecontrollers">IVdsLun::QueryActiveControllers</a> 
    method to query controller associations. Use the 
    <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontroller-queryassociatedluns">IVdsController::QueryAssociatedLuns</a> 
    method to query the LUNs associated with a particular controller.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontroller-queryassociatedluns">IVdsController::QueryAssociatedLuns</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a>



<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdslun">IVdsLun</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-queryactivecontrollers">IVdsLun::QueryActiveControllers</a>
