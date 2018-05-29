---
UID: NS:cfgmgr32.BusNumber_Resource_s
title: BusNumber_Resource_s
author: windows-sdk-content
description: The BUSNUMBER_RESOURCE structure specifies either a resource list or a resource requirements list that describes bus number usage for a device instance. For more information about resource lists and resource requirements lists, see Hardware Resources.
old-location: devinst\busnumber_resource.htm
old-project: devinst
ms.assetid: 8dbf5499-8e43-4db9-b0ec-6536f1c6121c
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*PBUSNUMBER_RESOURCE, BUSNUMBER_RESOURCE, BUSNUMBER_RESOURCE structure [Device and Driver Installation], BusNumber_Resource_s, PBUSNUMBER_RESOURCE, PBUSNUMBER_RESOURCE structure pointer [Device and Driver Installation], cfgmgr32/BUSNUMBER_RESOURCE, cfgmgr32/PBUSNUMBER_RESOURCE, cfgmgrst_5fb3a498-87c1-40c1-8169-4348f2fabe03.xml, devinst.busnumber_resource"
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
req.typenames: BUSNUMBER_RESOURCE, *PBUSNUMBER_RESOURCE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	cfgmgr32.h
api_name:
-	BUSNUMBER_RESOURCE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# BusNumber_Resource_s structure


## -description


The BUSNUMBER_RESOURCE structure specifies either a resource list or a resource requirements list that describes bus number usage for a device instance. For more information about resource lists and resource requirements lists, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff547012">Hardware Resources</a>.


## -struct-fields




### -field BusNumber_Header

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff537825">BUSNUMBER_DES</a> structure.


### -field BusNumber_Data





#### For a resource list:

Zero.



#### For a resource requirements list:

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff537831">BUSNUMBER_RANGE</a> array.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff537825">BUSNUMBER_DES</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff537831">BUSNUMBER_RANGE</a>
 

 

