---
UID: NF:vds.IVdsSubSystemIscsi.CreateTarget
title: IVdsSubSystemIscsi::CreateTarget
author: windows-sdk-content
description: Creates an iSCSI target.
old-location: base\ivdssubsystemiscsi_createtarget.htm
tech.root: VDS
ms.assetid: 084a1f0e-0764-404a-bd9a-a724e4f12c5f
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CreateTarget, CreateTarget method [VDS], CreateTarget method [VDS],IVdsSubSystemIscsi interface, IVdsSubSystemIscsi interface [VDS],CreateTarget method, IVdsSubSystemIscsi.CreateTarget, IVdsSubSystemIscsi::CreateTarget, base.ivdssubsystemiscsi_createtarget, vds/IVdsSubSystemIscsi::CreateTarget, vdshwprv/IVdsSubSystemIscsi::CreateTarget
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vds.h
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
---

# IVdsSubSystemIscsi::CreateTarget


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Creates an iSCSI target. The interface pointer for the new 
   target object can be retrieved by calling 
   <a href="https://msdn.microsoft.com/1bb30247-efb8-488f-b142-8912c351f5f2">IVdsAsync::Wait</a> through the 
   <i>ppAsync</i> parameter. The 
   <a href="https://msdn.microsoft.com/21771c6a-eca9-47f3-b6fc-383bca1e11bf">VDS_ASYNC_OUTPUT</a> structure returned contains the target 
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

The address of an <a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a> interface pointer, which 
      VDS initializes on return.  Callers must release the interface.  Use this interface to cancel, wait for, or 
      query the status of the operation. If you call 
      <a href="https://msdn.microsoft.com/1bb30247-efb8-488f-b142-8912c351f5f2">IVdsAsync::Wait</a> on this method and a success HRESULT value is returned, you must release the 
      interfaces returned in the <a href="https://msdn.microsoft.com/21771c6a-eca9-47f3-b6fc-383bca1e11bf">VDS_ASYNC_OUTPUT</a> structure by calling the <a href="_com_iunknown_release">IUnknown::Release</a> method on each interface pointer. However, if <b>Wait</b> returns a failure HRESULT value, or if the <i>pHrResult</i> parameter of <b>Wait</b> receives a failure HRESULT value, the interface pointers in the <b>VDS_ASYNC_OUTPUT</b> structure are <b>NULL</b> and do not need to be released. You can test for success or failure HRESULT values by using the <a href="_com_succeeded">SUCCEEDED</a> and <a href="_com_failed">FAILED</a> macros defined in Winerror.h.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="_com_hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

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
The subsystem object does not support this method. This indicates that the hardware provider has set the VDS_SF_SUPPORTS_SIMPLE_TARGET_CONFIG flag in the <b>ulFlags</b> member of the <a href="https://msdn.microsoft.com/8fecb874-5c59-4f55-b528-040ff9209612">VDS_SUB_SYSTEM_PROP</a> structure for the subsystem object.

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
        <a href="https://msdn.microsoft.com/aeb06a98-8896-446f-abd5-ea40be0bea40">IVdsHwProvider::Reenumerate</a> method 
        followed by the  <a href="https://msdn.microsoft.com/25ddc73c-5d1b-4bec-bbc2-9f22a5f82ffe">IVdsHwProvider::Refresh</a> 
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




<a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a>



<a href="https://msdn.microsoft.com/eb80020b-caf8-4d85-b250-d9a8738b8848">IVdsLunIscsi::AssociateTargets</a>



<a href="https://msdn.microsoft.com/cbcf1e14-7e3d-44e6-8c4a-afe927ed0f9d">IVdsSubSystem::GetProperties</a>



<a href="https://msdn.microsoft.com/e92417b7-6664-4fd7-900f-aedc83291dea">IVdsSubSystemIscsi</a>



<a href="https://msdn.microsoft.com/21771c6a-eca9-47f3-b6fc-383bca1e11bf">VDS_ASYNC_OUTPUT</a>



<a href="https://msdn.microsoft.com/17a07d21-a10a-4f18-a975-def6db073256">VDS_SUB_SYSTEM_FLAG</a>



<a href="https://msdn.microsoft.com/8fecb874-5c59-4f55-b528-040ff9209612">VDS_SUB_SYSTEM_PROP</a>
 

 

