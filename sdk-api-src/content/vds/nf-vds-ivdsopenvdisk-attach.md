---
UID: NF:vds.IVdsOpenVDisk.Attach
title: IVdsOpenVDisk::Attach
author: windows-sdk-content
description: Attaches a virtual disk.
old-location: base\ivdsopenvdisk_attach.htm
tech.root: vds
ms.assetid: 02647fe6-b94c-43ac-939c-262cea2c49d4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ATTACH_VIRTUAL_DISK_FLAG_NONE, ATTACH_VIRTUAL_DISK_FLAG_NO_DRIVE_LETTER, ATTACH_VIRTUAL_DISK_FLAG_NO_LOCAL_HOST, ATTACH_VIRTUAL_DISK_FLAG_PERMANENT_LIFETIME, ATTACH_VIRTUAL_DISK_FLAG_READ_ONLY, Attach, Attach method, Attach method,IVdsOpenVDisk interface, IVdsOpenVDisk interface,Attach method, IVdsOpenVDisk.Attach, IVdsOpenVDisk::Attach, base.ivdsopenvdisk_attach, vds/IVdsOpenVDisk::Attach
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsOpenVDisk.Attach
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsOpenVDisk::Attach


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Attaches a virtual disk.


## -parameters




### -param pStringSecurityDescriptor [in]

A string that contains the security descriptor for the virtual disk. If not specified, the security descriptor in use is: "D:P(A;;GA;;;WD)" on Windows 7, and "D:P(A;;GA;;;WD)(A;;GA;;;AC)" on Windows 8.1 and later.


### -param Flags [in]

A bitmask  of  <a href="vhd.surface_virtual_disk_flag">ATTACH_VIRTUAL_DISK_FLAG</a> enumeration values specifying how the virtual disk is to be attached. Possible values include the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ATTACH_VIRTUAL_DISK_FLAG_NONE"></a><a id="attach_virtual_disk_flag_none"></a><dl>
<dt><b>ATTACH_VIRTUAL_DISK_FLAG_NONE</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
No flags are specified.

</td>
</tr>
<tr>
<td width="40%"><a id="ATTACH_VIRTUAL_DISK_FLAG_READ_ONLY"></a><a id="attach_virtual_disk_flag_read_only"></a><dl>
<dt><b>ATTACH_VIRTUAL_DISK_FLAG_READ_ONLY</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Attach the virtual disk as read-only.

</td>
</tr>
<tr>
<td width="40%"><a id="ATTACH_VIRTUAL_DISK_FLAG_NO_DRIVE_LETTER"></a><a id="attach_virtual_disk_flag_no_drive_letter"></a><dl>
<dt><b>ATTACH_VIRTUAL_DISK_FLAG_NO_DRIVE_LETTER</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Mount all volumes on the attached virtual disk without assigning drive letters to them.

</td>
</tr>
<tr>
<td width="40%"><a id="ATTACH_VIRTUAL_DISK_FLAG_PERMANENT_LIFETIME"></a><a id="attach_virtual_disk_flag_permanent_lifetime"></a><dl>
<dt><b>ATTACH_VIRTUAL_DISK_FLAG_PERMANENT_LIFETIME</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The VDS service automatically  sets this flag so that the VHD remains attached until the <a href="https://msdn.microsoft.com/b720f6fc-f6a0-4cda-b710-30941bb79a06">IVdsOpenVDisk::Detach</a> method is called to detach it.

</td>
</tr>
<tr>
<td width="40%"><a id="ATTACH_VIRTUAL_DISK_FLAG_NO_LOCAL_HOST"></a><a id="attach_virtual_disk_flag_no_local_host"></a><dl>
<dt><b>ATTACH_VIRTUAL_DISK_FLAG_NO_LOCAL_HOST</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Reserved. Do not use.

</td>
</tr>
</table>
 


### -param ProviderSpecificFlags [in]

A bitmask of flags that are specific to the type of virtual disk that is being attached. These flags are provider-specific. For the Microsoft virtual disk provider, this parameter must be zero.


### -param TimeoutInMs [in]

This parameter is reserved for future use.


### -param ppAsync [out]

A pointer to an <a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a> interface that upon successful completion receives the <b>IVdsAsync</b> interface to monitor and control this operation.  Callers must release the interface received when they have finished with it.  If the <a href="https://msdn.microsoft.com/1bb30247-efb8-488f-b142-8912c351f5f2">IVdsAsync::Wait</a> method is called on the interface and a success HRESULT value is returned, the interfaces returned in the <a href="https://msdn.microsoft.com/21771c6a-eca9-47f3-b6fc-383bca1e11bf">VDS_ASYNC_OUTPUT</a> structure must be released by calling the <a href="_com_iunknown_release">IUnknown::Release</a> method on each interface pointer. However, if <b>Wait</b> returns a failure HRESULT value, or if the <i>pHrResult</i> parameter of <b>Wait</b> receives a failure HRESULT value, the interface pointers in the <b>VDS_ASYNC_OUTPUT</b> structure are <b>NULL</b> and do not need to be released. You can test for success or failure HRESULT values by using the <a href="_com_succeeded">SUCCEEDED</a> and <a href="_com_failed">FAILED</a> macros defined in Winerror.h.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="_com_hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

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



When a virtual disk is attached, the caller can receive one or all of the following notifications:

<ul>
<li>If the caller is registered for VDS notifications, the caller receives a disk arrival notification. For more information, see <a href="https://msdn.microsoft.com/a0841215-3eb0-4769-b320-4da25b535362">VDS Notifications</a>.</li>
<li>If the caller is registered for PnP notifications, the caller receives a PnP disk arrival notification. For more information, see <a href="https://msdn.microsoft.com/82094d95-9af3-4222-9c5e-ce2df9bab5e3">RegisterDeviceNotification</a>.</li>
</ul>
Applications must initialize process-wide security by calling the <a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a> function. The <i>dwImpLevel</i> parameter should be set to <b>RPC_C_IMP_LEVEL_IMPERSONATE</b>.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>These actions are not required until Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/3d5f080f-3e83-437e-8cbc-9730988f5dcc">IVdsOpenVDisk</a>
 

 

