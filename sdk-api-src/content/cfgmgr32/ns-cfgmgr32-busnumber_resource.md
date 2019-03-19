---
UID: NS:cfgmgr32.BusNumber_Resource_s
title: BUSNUMBER_RESOURCE (cfgmgr32.h)
author: windows-sdk-content
description: The BUSNUMBER_RESOURCE structure specifies either a resource list or a resource requirements list that describes bus number usage for a device instance. For more information about resource lists and resource requirements lists, see Hardware Resources.
old-location: devinst\busnumber_resource.htm
tech.root: devinst
ms.assetid: 8dbf5499-8e43-4db9-b0ec-6536f1c6121c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PBUSNUMBER_RESOURCE, BUSNUMBER_RESOURCE, BUSNUMBER_RESOURCE structure [Device and Driver Installation], PBUSNUMBER_RESOURCE, PBUSNUMBER_RESOURCE structure pointer [Device and Driver Installation], cfgmgr32/BUSNUMBER_RESOURCE, cfgmgr32/PBUSNUMBER_RESOURCE, cfgmgrst_5fb3a498-87c1-40c1-8169-4348f2fabe03.xml, devinst.busnumber_resource"
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
 - BUSNUMBER_RESOURCE
product: Windows
targetos: Windows
req.typenames: BUSNUMBER_RESOURCE, *PBUSNUMBER_RESOURCE
req.redist: 
---

# BUSNUMBER_RESOURCE structure


## -description


The BUSNUMBER_RESOURCE structure specifies either a resource list or a resource requirements list that describes bus number usage for a device instance. For more information about resource lists and resource requirements lists, see <a href="https://msdn.microsoft.com/c7a6997b-34f9-4dd9-b384-2321a8b5ce54">Hardware Resources</a>.


## -struct-fields




### -field BusNumber_Header

A <a href="https://msdn.microsoft.com/3007e271-fe78-404c-ba97-ceb0be334592">BUSNUMBER_DES</a> structure.


### -field BusNumber_Data





#### For a resource list:

Zero.



#### For a resource requirements list:

A <a href="https://msdn.microsoft.com/00b9bcd3-f1fe-4853-a6fb-0ac8b1fffa1b">BUSNUMBER_RANGE</a> array.


## -see-also




<a href="https://msdn.microsoft.com/3007e271-fe78-404c-ba97-ceb0be334592">BUSNUMBER_DES</a>



<a href="https://msdn.microsoft.com/00b9bcd3-f1fe-4853-a6fb-0ac8b1fffa1b">BUSNUMBER_RANGE</a>
 

 

