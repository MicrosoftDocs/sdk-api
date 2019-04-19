---
UID: NS:cfgmgr32.IO_Resource_s
title: IO_RESOURCE (cfgmgr32.h)
author: windows-sdk-content
description: The IO_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes I/O port usage for a device instance.
old-location: devinst\io_resource.htm
tech.root: devinst
ms.assetid: d18a1f92-b76c-4240-9a0e-7474c258436c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PIO_RESOURCE, IO_RESOURCE, IO_RESOURCE structure [Device and Driver Installation], PIO_RESOURCE, PIO_RESOURCE structure pointer [Device and Driver Installation], cfgmgr32/IO_RESOURCE, cfgmgr32/PIO_RESOURCE, cfgmgrst_4016b1e2-26af-4ccb-b2d9-823e0c4bf66c.xml, devinst.io_resource"
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: IO_RESOURCE, *PIO_RESOURCE
req.redist: 
ms.custom: 19H1
---

# IO_RESOURCE structure


## -description


The IO_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes I/O port usage for a device instance. For more information about resource lists and resource requirements lists, see <a href="https://msdn.microsoft.com/c7a6997b-34f9-4dd9-b384-2321a8b5ce54">Hardware Resources</a>.


## -struct-fields




### -field IO_Header

An <a href="https://msdn.microsoft.com/4b2ae544-0254-4221-80df-e2df4a23d15f">IO_DES</a> structure.


### -field IO_Data





#### For a resource list:

Zero.



#### For a resource requirements list:

An <a href="https://msdn.microsoft.com/1793684b-b4c4-4467-9ac9-8c6b1eea65e3">IO_RANGE</a> array.


## -see-also




<a href="https://msdn.microsoft.com/4b2ae544-0254-4221-80df-e2df4a23d15f">IO_DES</a>



<a href="https://msdn.microsoft.com/1793684b-b4c4-4467-9ac9-8c6b1eea65e3">IO_RANGE</a>
 

 

