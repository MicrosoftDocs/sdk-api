---
UID: NF:virtdisk.DetachVirtualDisk
title: DetachVirtualDisk function (virtdisk.h)
description: Detaches a virtual hard disk (VHD) or CD or DVD image file (ISO) by locating an appropriate virtual disk provider to accomplish the operation.
helpviewer_keywords: ["DetachVirtualDisk","DetachVirtualDisk function [VHD]","vdssys/DetachVirtualDisk","vhd.detachvirtualdisk","vhd.unsurfacevirtualdisk","virtdisk/DetachVirtualDisk"]
old-location: vhd\detachvirtualdisk.htm
tech.root: VStor
ms.assetid: 9b3874e1-e107-42f8-9ede-eb1eb6164ed2
ms.date: 12/05/2018
ms.keywords: DetachVirtualDisk, DetachVirtualDisk function [VHD], vdssys/DetachVirtualDisk, vhd.detachvirtualdisk, vhd.unsurfacevirtualdisk, virtdisk/DetachVirtualDisk
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
 - DetachVirtualDisk
 - virtdisk/DetachVirtualDisk
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
 - DetachVirtualDisk
---

# DetachVirtualDisk function


## -description

Detaches a virtual hard disk (VHD) or CD or DVD image file (ISO) by locating an appropriate virtual 
    disk provider to accomplish the operation.

## -parameters

### -param VirtualDiskHandle [in]

A handle to an open virtual disk, which must have been opened using the 
      <b>VIRTUAL_DISK_ACCESS_DETACH</b> flag set in the 
      <i>VirtualDiskAccessMask</i> parameter to the 
      <a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk">OpenVirtualDisk</a> function. For information on how to 
      open a virtual disk, see the <b>OpenVirtualDisk</b> 
      function.

### -param Flags [in]

A valid combination of values of the 
      <a href="/windows/win32/api/virtdisk/ne-virtdisk-detach_virtual_disk_flag">DETACH_VIRTUAL_DISK_FLAG</a> enumeration.

### -param ProviderSpecificFlags [in]

Flags specific to the type of virtual disk being detached. May be zero if none are required.

## -returns

Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is an error code. For more information, see 
       <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

If the <b>DetachVirtualDisk</b> function fails with an 
    error code value of <b>ERROR_INVALID_PARAMETER</b>, the cause may be due to any of the 
    following conditions:

<ul>
<li>The <i>VirtualDiskHandle</i> parameter is not a valid handle created by the 
      <a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk">OpenVirtualDisk</a> function.</li>
<li>The <i>Flags</i> parameter is set to a value other than 
      <b>DETACH_VIRTUAL_DISK_FLAG_NONE</b> (0).</li>
</ul>
The host volume that contains the virtual disk image file cannot be compressed or EFS encrypted.

All other open handles to the virtual disk must be closed before the 
    <b>DetachVirtualDisk</b> function can succeed.

If the virtual disk is attached and another handle that was used to attach it has 
    been closed, this is because the <b>ATTACH_VIRTUAL_DISK_FLAG_PERMANENT_LIFETIME</b> flag was 
    specified. In this case, the <b>DetachVirtualDisk</b> 
    function can succeed but the VHD will remain attached. If the 
    <b>ATTACH_VIRTUAL_DISK_FLAG_PERMANENT_LIFETIME</b> was not specified, the virtual disk will be 
    automatically detached when the last open handle is closed.

This function will fail if a provider cannot be found, if the image file is not valid, if the image is not 
    attached, or if the caller does not have <b>SE_MANAGE_VOLUME_PRIVILEGE</b> access rights on a 
    Windows Server operating system. For more information about file security, see 
    <a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>.

CD and DVD image files (ISO) are not supported before Windows 8 and 
    Windows Server 2012.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



<a href="/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>