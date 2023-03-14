---
UID: NF:vds.IVdsController.SetStatus
title: IVdsController::SetStatus (vds.h)
description: The IVdsController::SetStatus (vds.h) method sets the status of a controller to the specified value.
helpviewer_keywords: ["IVdsController interface [VDS]","SetStatus method","IVdsController.SetStatus","IVdsController::SetStatus","SetStatus","SetStatus method [VDS]","SetStatus method [VDS]","IVdsController interface","base.ivdscontroller_setstatus","vds/IVdsController::SetStatus","vdshwprv/IVdsController::SetStatus"]
old-location: base\ivdscontroller_setstatus.htm
tech.root: base
ms.assetid: f9bae451-ef47-46ad-a11e-b7b36a031a8a
ms.date: 08/05/2022
ms.keywords: IVdsController interface [VDS],SetStatus method, IVdsController.SetStatus, IVdsController::SetStatus, SetStatus, SetStatus method [VDS], SetStatus method [VDS],IVdsController interface, base.ivdscontroller_setstatus, vds/IVdsController::SetStatus, vdshwprv/IVdsController::SetStatus
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
 - IVdsController::SetStatus
 - vds/IVdsController::SetStatus
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
 - IVdsController.SetStatus
---

# IVdsController::SetStatus


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Sets the status of a 
   controller to the specified value.

## -parameters

### -param status [in]

Values enumerated by <a href="/windows/desktop/api/vds/ne-vds-vds_controller_status">VDS_CONTROLLER_STATUS</a>. 
      Callers can pass in a subset of the possible enumeration values. Passing in 
      <b>VDS_CS_UNKNOWN</b> returns <b>E_INVALIDARG</b>.

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
This return value signals a software or communication problem inside a provider that caches information about 
        the array. Use the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a> 
        method followed by the 
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
The controller object is no longer present.

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
The controller is in a failed state and is unable to perform the requested operation.

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
Another operation is in progress; this operation cannot proceed until the previous operation or operations 
        are complete.
       

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

This method enables you to set the status of a single controller. You can set the status of all the controllers 
    in a subsystem at once by calling the 
    <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-setcontrollerstatus">IVdsSubSystem::SetControllerStatus</a> 
    method. Use the 
    <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontroller-getproperties">IVdsController::GetProperties</a> 
    method to get the current status of the controller.
   

Implementers are responsible for performing any necessary operations to get the status to the specified state. 
    For example, if the caller passes in <b>VDS_CS_OFFLINE</b> as the controller status, you might 
    need to first clear the cache for the controller.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdscontroller">IVdsController</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontroller-getproperties">IVdsController::GetProperties</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-setcontrollerstatus">IVdsSubSystem::SetControllerStatus</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_controller_status">VDS_CONTROLLER_STATUS</a>
