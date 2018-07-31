---
UID: NF:vds.IVdsVdProvider.CreateVDisk
title: IVdsVdProvider::CreateVDisk
author: windows-sdk-content
description: Creates a virtual disk.
old-location: base\ivdsvdprovider_createdisk.htm
old-project: VDS
ms.assetid: 3655946d-f8b5-46a1-97e3-82b0831124b3
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CREATE_VIRTUAL_DISK_FLAG_FULL_PHYSICAL_ALLOCATION, CREATE_VIRTUAL_DISK_FLAG_NONE, CreateVDisk, CreateVDisk method, CreateVDisk method,IVdsVdProvider interface, IVdsVdProvider interface,CreateVDisk method, IVdsVdProvider.CreateVDisk, IVdsVdProvider::CreateVDisk, base.ivdsvdprovider_createdisk, vds/IVdsVdProvider::CreateVDisk
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VDS_VOLUME_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsVdProvider.CreateVDisk
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsVdProvider::CreateVDisk


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Creates a virtual disk.


## -parameters




### -param VirtualDeviceType [in]

A pointer to a <a href="https://msdn.microsoft.com/9f0c1848-fa8e-4747-a3b1-71a274695280">VIRTUAL_STORAGE_TYPE</a> structure that specifies the type of virtual disk to be created.


### -param pPath [in]

A <b>NULL</b>-terminated wide-character string containing the name and directory path for the backing file to be created for the virtual disk.


### -param pStringSecurityDescriptor [in]

A <b>NULL</b>-terminated wide-character string containing the security descriptor to be applied to
    the virtual disk. If this parameter is <b>NULL</b>, the security descriptor in the caller's access token will be used.


### -param Flags [in]

A bitmask of <a href="https://msdn.microsoft.com/35dba6c6-2825-425a-b432-a6ac8ad4ea4b">CREATE_VIRTUAL_DISK_FLAG</a> enumeration values specifying how the virtual disk is to be created.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CREATE_VIRTUAL_DISK_FLAG_NONE"></a><a id="create_virtual_disk_flag_none"></a><dl>
<dt><b>CREATE_VIRTUAL_DISK_FLAG_NONE</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
No flags are specified.

</td>
</tr>
<tr>
<td width="40%"><a id="CREATE_VIRTUAL_DISK_FLAG_FULL_PHYSICAL_ALLOCATION"></a><a id="create_virtual_disk_flag_full_physical_allocation"></a><dl>
<dt><b>CREATE_VIRTUAL_DISK_FLAG_FULL_PHYSICAL_ALLOCATION</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Pre-allocate all physical space necessary for the virtual size of the virtual disk. This flag is valid only for a fixed-size virtual disk.

</td>
</tr>
</table>
 


### -param ProviderSpecificFlags [in]

A bitmask of flags that are specific to the type of virtual disk that is being created. These flags are provider-specific. For the Microsoft virtual disk provider, this parameter must be zero.


### -param Reserved [in]

The parameter is reserved and must be zero.


### -param pCreateDiskParameters [in]

A pointer to a <a href="https://msdn.microsoft.com/7ee830d5-6392-4e66-a8bb-2fd92c1e092c">VDS_CREATE_VDISK_PARAMETERS</a> structure that contains the virtual disk creation parameters.


### -param ppAsync [out]

A pointer to an <a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a> interface that upon successful completion receives the <b>IVdsAsync</b> interface to monitor and control this operation.  Callers must release the interface received when they are done with it.  If the <a href="https://msdn.microsoft.com/1bb30247-efb8-488f-b142-8912c351f5f2">IVdsAsync::Wait</a> method is called on the interface and a success HRESULT value is returned, the interfaces returned in the <a href="https://msdn.microsoft.com/21771c6a-eca9-47f3-b6fc-383bca1e11bf">VDS_ASYNC_OUTPUT</a> structure must be released by calling the <a href="_com_iunknown_release">IUnknown::Release</a> method on each interface pointer. However, if <b>Wait</b> returns a failure HRESULT value, or if the <i>pHrResult</i> parameter of <b>Wait</b> receives a failure HRESULT value, the interface pointers in the <b>VDS_ASYNC_OUTPUT</b> structure are <b>NULL</b> and do not need to be released. You can test for success or failure HRESULT values by using the <a href="_com_succeeded">SUCCEEDED</a> and <a href="_com_failed">FAILED</a> macros defined in Winerror.h.


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



Applications must initialize process-wide security by calling the <a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a> function. The <i>dwImpLevel</i> parameter should be set to <b>RPC_C_IMP_LEVEL_IMPERSONATE</b>.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>These actions are not required until Windows 7 and Windows Server 2008 R2.

If the virtual disk with the specified file name does not exist, it is created. If the virtual disk already exists, the virtual disk provider returns an interface pointer to the existing virtual disk object without re-creating the file.




## -see-also




<a href="https://msdn.microsoft.com/812e8ac5-91c5-455a-94e7-2edf55d92cdc">IVdsVdProvider</a>
 

 

