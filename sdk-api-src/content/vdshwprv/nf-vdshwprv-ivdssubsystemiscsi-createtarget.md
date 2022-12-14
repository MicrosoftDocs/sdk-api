---
UID: NF:vdshwprv.IVdsSubSystemIscsi.CreateTarget
title: IVdsSubSystemIscsi::CreateTarget (vdshwprv.h)
description: The IVdsSubSystemIscsi::CreateTarget (vdshwprv.h) method creates an iSCSI target.
helpviewer_keywords: ["CreateTarget","CreateTarget method [VDS]","CreateTarget method [VDS]","IVdsSubSystemIscsi interface","IVdsSubSystemIscsi interface [VDS]","CreateTarget method","IVdsSubSystemIscsi.CreateTarget","IVdsSubSystemIscsi::CreateTarget","base.ivdssubsystemiscsi_createtarget","vds/IVdsSubSystemIscsi::CreateTarget","vdshwprv/IVdsSubSystemIscsi::CreateTarget"]
old-location: base\ivdssubsystemiscsi_createtarget.htm
tech.root: base
ms.assetid: 084a1f0e-0764-404a-bd9a-a724e4f12c5f
ms.date: 08/08/2022
ms.keywords: CreateTarget, CreateTarget method [VDS], CreateTarget method [VDS],IVdsSubSystemIscsi interface, IVdsSubSystemIscsi interface [VDS],CreateTarget method, IVdsSubSystemIscsi.CreateTarget, IVdsSubSystemIscsi::CreateTarget, base.ivdssubsystemiscsi_createtarget, vds/IVdsSubSystemIscsi::CreateTarget, vdshwprv/IVdsSubSystemIscsi::CreateTarget
req.header: vdshwprv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
req.redist: VDS 1.1
ms.custom: 19H1
f1_keywords:
 - IVdsSubSystemIscsi::CreateTarget
 - vdshwprv/IVdsSubSystemIscsi::CreateTarget
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
 - IVdsSubSystemIscsi.CreateTarget
---

# IVdsSubSystemIscsi::CreateTarget


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Creates an iSCSI target. The interface pointer for the new 
   target object can be retrieved by calling 
   <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsasync-wait">IVdsAsync::Wait</a> through the 
   <i>ppAsync</i> parameter. The 
   <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_async_output">VDS_ASYNC_OUTPUT</a> structure returned contains the target 
   object interface pointer in the <b>ct.pTargetUnk</b> member.

## -parameters

### -param pwszIscsiName [in]

A string specifying the iSCSI name to assign to the target.  The target name must be unique across all 
      targets in all subsystems visible on the network.
      

If <i>pwszIscsiName</i> is <b>NULL</b> or points to an empty string, 
       the provider will generate the iSCSI name to assign to the target.

### -param pwszFriendlyName [in]

A string specifying the friendly name to assign to the target.  This corresponds to the iSCSI alias.

### -param ppAsync [out]

The address of an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> interface pointer, which 
      VDS initializes on return.  Callers must release the interface.  Use this interface to cancel, wait for, or 
      query the status of the operation. If you call 
      <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsasync-wait">IVdsAsync::Wait</a> on this method and a success HRESULT value is returned, you must release the 
      interfaces returned in the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_async_output">VDS_ASYNC_OUTPUT</a> structure by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method on each interface pointer. However, if <b>Wait</b> returns a failure HRESULT value, or if the <i>pHrResult</i> parameter of <b>Wait</b> receives a failure HRESULT value, the interface pointers in the <b>VDS_ASYNC_OUTPUT</b> structure are <b>NULL</b> and do not need to be released. You can test for success or failure HRESULT values by using the <a href="/windows/desktop/api/winerror/nf-winerror-succeeded">SUCCEEDED</a> and <a href="/windows/desktop/api/winerror/nf-winerror-failed">FAILED</a> macros defined in Winerror.h.

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
The target was created successfully.

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
The subsystem object does not support this method. This indicates that the hardware provider has set the VDS_SF_SUPPORTS_SIMPLE_TARGET_CONFIG flag in the <b>ulFlags</b> member of the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_sub_system_prop">VDS_SUB_SYSTEM_PROP</a> structure for the subsystem object.

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
The cache of the provider is corrupted. This indicates a software or communication problem inside a 
        provider that caches information about the attached devices. The caller can use the 
        <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a> method 
        followed by the  <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> 
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
Another operation is in progress. This operation cannot proceed until previous operations are complete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_NAME_NOT_UNIQUE</b></dt>
<dt>0x80042701L</dt>
</dl>
</td>
<td width="60%">
A non-unique name was specified in the <i>pwszIscsiName</i> parameter.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsluniscsi-associatetargets">IVdsLunIscsi::AssociateTargets</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-getproperties">IVdsSubSystem::GetProperties</a>



<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdssubsystemiscsi">IVdsSubSystemIscsi</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_async_output">VDS_ASYNC_OUTPUT</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_sub_system_flag">VDS_SUB_SYSTEM_FLAG</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_sub_system_prop">VDS_SUB_SYSTEM_PROP</a>
