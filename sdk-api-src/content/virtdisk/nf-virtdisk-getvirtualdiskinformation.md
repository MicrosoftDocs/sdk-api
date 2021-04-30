---
UID: NF:virtdisk.GetVirtualDiskInformation
title: GetVirtualDiskInformation function (virtdisk.h)
description: Retrieves information about a VHD.
helpviewer_keywords: ["GetVirtualDiskInformation","GetVirtualDiskInformation function [VHD]","vdssys/GetVirtualDiskInformation","vhd.getvirtualdiskinformation","virtdisk/GetVirtualDiskInformation"]
old-location: vhd\getvirtualdiskinformation.htm
tech.root: VStor
ms.assetid: c3832be0-e9b8-4f6a-a663-06349c7fd639
ms.date: 12/05/2018
ms.keywords: GetVirtualDiskInformation, GetVirtualDiskInformation function [VHD], vdssys/GetVirtualDiskInformation, vhd.getvirtualdiskinformation, virtdisk/GetVirtualDiskInformation
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
 - GetVirtualDiskInformation
 - virtdisk/GetVirtualDiskInformation
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
 - GetVirtualDiskInformation
---

# GetVirtualDiskInformation function


## -description

Retrieves information about a virtual hard disk (VHD).

## -parameters

### -param VirtualDiskHandle [in]

A handle to the open VHD, which must have been opened using the 
      <b>VIRTUAL_DISK_ACCESS_GET_INFO</b> flag set in the 
      <i>VirtualDiskAccessMask</i> parameter to the 
      <a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk">OpenVirtualDisk</a> function. For information on how to 
      open a VHD, see the <b>OpenVirtualDisk</b> function.

### -param VirtualDiskInfoSize [in, out]

A pointer to a <b>ULONG</b> that contains the size of the 
      <i>VirtualDiskInfo</i> parameter.

### -param VirtualDiskInfo [in, out]

A pointer to a valid [GET_VIRTUAL_DISK_INFO](./ns-virtdisk-get_virtual_disk_info.md) 
      structure. The format of the data returned is dependent on the value passed in the 
      <b>Version</b> member by the caller.

### -param SizeUsed [in, out, optional]

A pointer to a <b>ULONG</b> that contains the size used.

## -returns

Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b> and the 
       <i>VirtualDiskInfo</i> parameter contains the requested information.

If the function fails, the return value is an error code and the <i>VirtualDiskInfo</i> 
       parameter is undefined. For more information, see 
       <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

The <b>GetVirtualDiskInformation</b> function 
    can be called on any valid <i>VirtualDiskHandle</i>, provided the handle was opened using the 
    <b>VIRTUAL_DISK_ACCESS_GET_INFO</b> flag. The VHD is not required to be an attached disk.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



[GET_VIRTUAL_DISK_INFO](./ns-virtdisk-get_virtual_disk_info.md)



<a href="/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>