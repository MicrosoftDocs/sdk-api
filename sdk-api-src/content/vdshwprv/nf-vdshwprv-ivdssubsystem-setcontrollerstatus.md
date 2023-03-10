---
UID: NF:vdshwprv.IVdsSubSystem.SetControllerStatus
title: IVdsSubSystem::SetControllerStatus (vdshwprv.h)
description: The IVdsSubSystem::SetControllerStatus (vdshwprv.h) method sets the status (either online or offline) of the controllers in the subsystem.
helpviewer_keywords: ["IVdsSubSystem interface [VDS]","SetControllerStatus method","IVdsSubSystem.SetControllerStatus","IVdsSubSystem::SetControllerStatus","SetControllerStatus","SetControllerStatus method [VDS]","SetControllerStatus method [VDS]","IVdsSubSystem interface","base.ivdssubsystem_setcontrollerstatus","vds/IVdsSubSystem::SetControllerStatus","vdshwprv/IVdsSubSystem::SetControllerStatus"]
old-location: base\ivdssubsystem_setcontrollerstatus.htm
tech.root: base
ms.assetid: 080a48a5-1c25-440a-ad3c-528cdaef40e9
ms.date: 08/08/2022
ms.keywords: IVdsSubSystem interface [VDS],SetControllerStatus method, IVdsSubSystem.SetControllerStatus, IVdsSubSystem::SetControllerStatus, SetControllerStatus, SetControllerStatus method [VDS], SetControllerStatus method [VDS],IVdsSubSystem interface, base.ivdssubsystem_setcontrollerstatus, vds/IVdsSubSystem::SetControllerStatus, vdshwprv/IVdsSubSystem::SetControllerStatus
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
 - IVdsSubSystem::SetControllerStatus
 - vdshwprv/IVdsSubSystem::SetControllerStatus
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
 - IVdsSubSystem.SetControllerStatus
---

# IVdsSubSystem::SetControllerStatus


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Sets 
   the status (either online or offline) of the controllers in the subsystem.

## -parameters

### -param pOnlineControllerIdArray [in]

Pointer to an array of controller GUIDs. The provider sets these controllers to online. This array includes 
      controllers already set to online that are to remain so.

### -param lNumberOfOnlineControllers [in]

The number of controllers specified in 
     <i>pOnlineControllersArray</i>.

### -param pOfflineControllerIdArray [in]

Pointer to an array of controller GUIDs. The provider sets these controllers to offline. This array includes 
      controllers already set to offline that are to remain so.

### -param lNumberOfOfflineControllers [in]

The number of controllers specified in <i>pOfflineControllersArray</i>.

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
Another operation is in progress; this operation cannot proceed until the previous operation or operations 
        are complete.
       

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
Can be returned from any method that takes a <b>VDS_OBJECT_ID</b> constant. This return 
        value indicates that the identifier does not refer to an existing object.

</td>
</tr>
</table>

## -remarks

This method enables a caller to set the status of all controllers at once. Use the 
    <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontroller-setstatus">IVdsController::SetStatus</a> method to set the 
    status of a single controller.

Callers must pass the complete set of controllers in either the <i>pOnlineControllerIdArray</i> 
    or <i>pOfflineControllerIdArray</i> parameter for each method call. The 
    <b>E_INVALIDARG</b> return value can indicate that not all controllers in the subsystem have 
    been specified in the arguments to this method.  
    The <b>SetControllerStatus</b> method requires that 
    all controllers in the subsystem be present in one of the two arrays supplied.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontroller-setstatus">IVdsController::SetStatus</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a>



<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdssubsystem">IVdsSubSystem</a>
