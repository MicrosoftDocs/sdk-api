---
UID: NF:vds.IVdsVdProvider.CreateVDisk
title: IVdsVdProvider::CreateVDisk (vds.h)
description: Creates a virtual disk.
helpviewer_keywords: ["CREATE_VIRTUAL_DISK_FLAG_FULL_PHYSICAL_ALLOCATION","CREATE_VIRTUAL_DISK_FLAG_NONE","CreateVDisk","CreateVDisk method","CreateVDisk method","IVdsVdProvider interface","IVdsVdProvider interface","CreateVDisk method","IVdsVdProvider.CreateVDisk","IVdsVdProvider::CreateVDisk","base.ivdsvdprovider_createdisk","vds/IVdsVdProvider::CreateVDisk"]
old-location: base\ivdsvdprovider_createdisk.htm
tech.root: base
ms.assetid: 3655946d-f8b5-46a1-97e3-82b0831124b3
ms.date: 12/05/2018
ms.keywords: CREATE_VIRTUAL_DISK_FLAG_FULL_PHYSICAL_ALLOCATION, CREATE_VIRTUAL_DISK_FLAG_NONE, CreateVDisk, CreateVDisk method, CreateVDisk method,IVdsVdProvider interface, IVdsVdProvider interface,CreateVDisk method, IVdsVdProvider.CreateVDisk, IVdsVdProvider::CreateVDisk, base.ivdsvdprovider_createdisk, vds/IVdsVdProvider::CreateVDisk
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsVdProvider::CreateVDisk
 - vds/IVdsVdProvider::CreateVDisk
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
 - IVdsVdProvider.CreateVDisk
---

# IVdsVdProvider::CreateVDisk


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Creates a virtual disk.

## -parameters

### -param VirtualDeviceType [in]

A pointer to a <a href="/windows/win32/api/virtdisk/ns-virtdisk-virtual_storage_type">VIRTUAL_STORAGE_TYPE</a> structure that specifies the type of virtual disk to be created.

### -param pPath [in]

A <b>NULL</b>-terminated wide-character string containing the name and directory path for the backing file to be created for the virtual disk.

### -param pStringSecurityDescriptor [in]

A <b>NULL</b>-terminated wide-character string containing the security descriptor to be applied to
    the virtual disk. If this parameter is <b>NULL</b>, the security descriptor in the caller's access token will be used.

### -param Flags [in]

A bitmask of <a href="/windows/win32/api/virtdisk/ne-virtdisk-create_virtual_disk_flag">CREATE_VIRTUAL_DISK_FLAG</a> enumeration values specifying how the virtual disk is to be created.

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

A pointer to a <a href="/windows/desktop/api/vds/ns-vds-vds_create_vdisk_parameters">VDS_CREATE_VDISK_PARAMETERS</a> structure that contains the virtual disk creation parameters.

### -param ppAsync [out]

A pointer to an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> interface that upon successful completion receives the <b>IVdsAsync</b> interface to monitor and control this operation.  Callers must release the interface received when they are done with it.  If the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsasync-wait">IVdsAsync::Wait</a> method is called on the interface and a success HRESULT value is returned, the interfaces returned in the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_async_output">VDS_ASYNC_OUTPUT</a> structure must be released by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method on each interface pointer. However, if <b>Wait</b> returns a failure HRESULT value, or if the <i>pHrResult</i> parameter of <b>Wait</b> receives a failure HRESULT value, the interface pointers in the <b>VDS_ASYNC_OUTPUT</b> structure are <b>NULL</b> and do not need to be released. You can test for success or failure HRESULT values by using the <a href="/windows/desktop/api/winerror/nf-winerror-succeeded">SUCCEEDED</a> and <a href="/windows/desktop/api/winerror/nf-winerror-failed">FAILED</a> macros defined in Winerror.h.

## -returns

This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

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

Applications must initialize process-wide security by calling the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a> function. The <i>dwImpLevel</i> parameter should be set to <b>RPC_C_IMP_LEVEL_IMPERSONATE</b>.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>These actions are not required until Windows 7 and Windows Server 2008 R2.

If the virtual disk with the specified file name does not exist, it is created. If the virtual disk already exists, the virtual disk provider returns an interface pointer to the existing virtual disk object without re-creating the file.

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsvdprovider">IVdsVdProvider</a>