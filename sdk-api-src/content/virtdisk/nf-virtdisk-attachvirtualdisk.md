---
UID: NF:virtdisk.AttachVirtualDisk
title: AttachVirtualDisk function (virtdisk.h)
description: Attaches a virtual hard disk (VHD) or CD or DVD image file (ISO) by locating an appropriate VHD provider to accomplish the attachment.
helpviewer_keywords: ["AttachVirtualDisk","AttachVirtualDisk function [VHD]","vdssys/AttachVirtualDisk","vhd.attachvirtualdisk","vhd.surfacevirtualdisk","virtdisk/AttachVirtualDisk"]
old-location: vhd\attachvirtualdisk.htm
tech.root: VStor
ms.assetid: 528370bc-77d4-4983-8910-d941165a037c
ms.date: 12/05/2018
ms.keywords: AttachVirtualDisk, AttachVirtualDisk function [VHD], vdssys/AttachVirtualDisk, vhd.attachvirtualdisk, vhd.surfacevirtualdisk, virtdisk/AttachVirtualDisk
req.header: virtdisk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: VirtDisk.lib
req.dll: VirtDisk.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AttachVirtualDisk
 - virtdisk/AttachVirtualDisk
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - VirtDisk.dll
api_name:
 - AttachVirtualDisk
---

# AttachVirtualDisk function


## -description

Attaches a virtual hard disk (VHD) or CD or DVD image file (ISO) by locating an appropriate VHD 
    provider to accomplish the attachment.

## -parameters

### -param VirtualDiskHandle [in]

A handle to an open virtual disk. For information on how to open a virtual disk, see the 
      <a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk">OpenVirtualDisk</a> function.

### -param SecurityDescriptor [in, optional]

An optional pointer to a 
      <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> to apply to the attached 
      virtual disk. If this parameter is <b>NULL</b>, the security descriptor of the virtual disk 
      image file is used.

Ensure that the security descriptor that <b>AttachVirtualDisk</b> applies to the attached virtual disk grants the write attributes permission for the user, or that the security descriptor of the virtual disk 
      image file grants the write attributes permission for the user  if you specify NULL for this parameter. If the security descriptor does not grant write attributes permission for a user, Shell displays the following error when the user accesses the attached virtual disk: <b>The Recycle Bin is corrupted. Do you want to empty the Recycle Bin for this drive?</b>

### -param Flags [in]

A valid combination of values of the 
      <a href="/windows/win32/api/virtdisk/ne-virtdisk-attach_virtual_disk_flag">ATTACH_VIRTUAL_DISK_FLAG</a> enumeration.

### -param ProviderSpecificFlags [in]

Flags specific to the type of virtual disk being attached. May be zero if none are required.

### -param Parameters [in, optional]

A pointer to a valid 
      <a href="/windows/win32/api/virtdisk/ns-virtdisk-attach_virtual_disk_parameters">ATTACH_VIRTUAL_DISK_PARAMETERS</a> 
      structure that contains attachment parameter data.

### -param Overlapped [in, optional]

An optional pointer to a valid <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> 
      structure if 
      <a href="/windows/desktop/Sync/synchronization-and-overlapped-input-and-output">asynchronous</a> operation is 
      desired.

## -returns

Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is an error code. For more information, see 
       <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

The <b>AttachVirtualDisk</b> function is not supported 
    for VHDs or ISOs hosted on Secure Digital (SD) media plugged into an SD controller in native mode (for which 
    sffdisk.sys, sffp_sd.sys, and sdbus.sys drivers would be loaded) and will 
    fail with the error <b>ERROR_FILE_NOT_FOUND</b>. VHDs and ISOs hosted on SD media connected to 
    a USB reader are supported.

If the <b>AttachVirtualDisk</b> function fails with an 
    error code value of <b>ERROR_INVALID_PARAMETER</b>, the cause may be due to any of the 
    following conditions:

<ul>
<li>The <i>VirtualDiskHandle</i> parameter is not a valid handle created by the 
      <a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk">OpenVirtualDisk</a> function.</li>
<li>The <i>Flags</i> parameter is set to a value larger than 
      <code>0x020</code>.</li>
<li>The <b>Version</b> member of the <i>Parameters</i> parameter is not 
      set to <b>ATTACH_VIRTUAL_DISK_VERSION_1</b>.</li>
</ul>
The host volume that contains the virtual disk image file cannot be compressed or EFS encrypted.

This function will fail if a provider cannot be found, if the VHD or ISO image file is not valid, if the VHD 
    image is already attached, or if the caller does not have <b>SE_MANAGE_VOLUME_PRIVILEGE</b> 
    access rights. For more information about file security, see 
    <a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>.

The intended access mode of the virtual disk must be considered when opening the virtual disk handle. For 
    example, if the virtual disk is being attached for read/write access, the 
    <i>VirtualDiskHandle</i> parameter must have been opened using the 
    <b>VIRTUAL_DISK_ACCESS_ATTACH_RW</b> access flag. For more information, see 
    <a href="/openspecs/windows_protocols/ms-vds/4fa2f54d-00b3-4cd9-b673-a6b8d64ed57f">VIRTUAL_DISK_ACCESS_MASK</a> and 
    <a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk">OpenVirtualDisk</a>.

CD and DVD image files (ISO) are not supported before Windows 8 and 
    Windows Server 2012.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



<a href="/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>

