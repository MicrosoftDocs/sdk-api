---
UID: NF:virtdisk.AddVirtualDiskParent
title: AddVirtualDiskParent function (virtdisk.h)
description: Attaches a parent to a virtual disk opened with the OPEN_VIRTUAL_DISK_FLAG_CUSTOM_DIFF_CHAIN flag.
helpviewer_keywords: ["AddVirtualDiskParent","AddVirtualDiskParent function [Virtual Storage]","virtdisk/AddVirtualDiskParent","vstor.addvirtualdiskparent"]
old-location: vstor\addvirtualdiskparent.htm
tech.root: VStor
ms.assetid: 1af2a21b-246e-42d0-a493-4c513e716dab
ms.date: 12/05/2018
ms.keywords: AddVirtualDiskParent, AddVirtualDiskParent function [Virtual Storage], virtdisk/AddVirtualDiskParent, vstor.addvirtualdiskparent
f1_keywords:
- virtdisk/AddVirtualDiskParent
dev_langs:
- c++
req.header: virtdisk.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- VirtDisk.dll
api_name:
- AddVirtualDiskParent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AddVirtualDiskParent function


## -description


Attaches a parent to a virtual disk opened with the 
    <b>OPEN_VIRTUAL_DISK_FLAG_CUSTOM_DIFF_CHAIN</b> flag.


## -parameters




### -param VirtualDiskHandle [in]

Handle to a virtual disk.


### -param ParentPath [in]

Address of a string containing a valid path to the virtual hard disk image to add as a parent.


## -returns



Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is an error code. For more information, see 
       <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">System Error Codes</a>.




## -remarks



This adds the specified parent virtual hard disk to the head of the differencing chain of the specified 
    virtual hard disk. If the differencing chain extends beyond the parent, this function can be called repeatedly to 
    add additional parents to the differencing chain.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd323699(v=vs.85)">VHD Functions</a>
 

 

