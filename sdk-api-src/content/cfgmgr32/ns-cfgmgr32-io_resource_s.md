---
UID: NS:cfgmgr32.IO_Resource_s
title: IO_Resource_s
author: windows-sdk-content
description: The IO_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes I/O port usage for a device instance.
old-location: devinst\io_resource.htm
old-project: devinst
ms.assetid: d18a1f92-b76c-4240-9a0e-7474c258436c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PIO_RESOURCE, IO_RESOURCE, IO_RESOURCE structure [Device and Driver Installation], IO_Resource_s, PIO_RESOURCE, PIO_RESOURCE structure pointer [Device and Driver Installation], cfgmgr32/IO_RESOURCE, cfgmgr32/PIO_RESOURCE, cfgmgrst_4016b1e2-26af-4ccb-b2d9-823e0c4bf66c.xml, devinst.io_resource"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: IO_RESOURCE, *PIO_RESOURCE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - cfgmgr32.h
api_name:
 - IO_RESOURCE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IO_Resource_s structure


## -description


The IO_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes I/O port usage for a device instance. For more information about resource lists and resource requirements lists, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff547012">Hardware Resources</a>.


## -struct-fields




### -field IO_Header

An <a href="https://msdn.microsoft.com/library/windows/hardware/ff548184">IO_DES</a> structure.


### -field IO_Data





#### For a resource list:

Zero.



#### For a resource requirements list:

An <a href="https://msdn.microsoft.com/library/windows/hardware/ff548192">IO_RANGE</a> array.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff548184">IO_DES</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff548192">IO_RANGE</a>
 

 

