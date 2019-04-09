---
UID: NS:virtdisk._RESIZE_VIRTUAL_DISK_PARAMETERS
title: RESIZE_VIRTUAL_DISK_PARAMETERS (virtdisk.h)
author: windows-sdk-content
description: Contains the parameters for a ResizeVirtualDisk function.
old-location: vstor\resize_virtual_disk_parameters.htm
tech.root: VStor
ms.assetid: ff44f07a-67d1-4ad3-be2b-0aea1d3c4a6a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PRESIZE_VIRTUAL_DISK_PARAMETERS, PRESIZE_VIRTUAL_DISK_PARAMETERS, PRESIZE_VIRTUAL_DISK_PARAMETERS structure pointer [Virtual Storage], RESIZE_VIRTUAL_DISK_PARAMETERS, RESIZE_VIRTUAL_DISK_PARAMETERS structure [Virtual Storage], _RESIZE_VIRTUAL_DISK_PARAMETERS, virtdisk/PRESIZE_VIRTUAL_DISK_PARAMETERS, virtdisk/RESIZE_VIRTUAL_DISK_PARAMETERS, vstor.resize_virtual_disk_parameters"
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VirtDisk.h
api_name:
 - RESIZE_VIRTUAL_DISK_PARAMETERS
product: Windows
targetos: Windows
req.typenames: RESIZE_VIRTUAL_DISK_PARAMETERS, *PRESIZE_VIRTUAL_DISK_PARAMETERS
req.redist: 
---

# RESIZE_VIRTUAL_DISK_PARAMETERS structure


## -description


Contains the parameters for a 
    <a href="https://msdn.microsoft.com/d000c03e-c0ad-4054-b2eb-1aca34a95816">ResizeVirtualDisk</a> function.


## -struct-fields




### -field Version

Discriminant for the union containing a value enumerated from the 
      <a href="https://msdn.microsoft.com/779381fb-4433-46c5-8caf-b830cd015c95">RESIZE_VIRTUAL_DISK_VERSION</a> 
      enumeration.


### -field Version1

If the <b>Version</b> member is 
       <b>RESIZE_VIRTUAL_DISK_VERSION_1</b> (1), this structure is used.


### -field Version1.NewSize

Contains the new size of the virtual disk.


## -see-also




<a href="https://msdn.microsoft.com/779381fb-4433-46c5-8caf-b830cd015c95">RESIZE_VIRTUAL_DISK_VERSION</a>



<a href="https://msdn.microsoft.com/d000c03e-c0ad-4054-b2eb-1aca34a95816">ResizeVirtualDisk</a>



<a href="https://msdn.microsoft.com/79c3b3ad-4eaf-49ce-a8ee-b26faf6c2cba">VHD Functions</a>
 

 

