---
UID: NS:cfgmgr32.BusNumber_Des_s
title: BusNumber_Des_s
author: windows-sdk-content
description: The BUSNUMBER_DES structure is used for specifying either a resource list or a resource requirements list that describes bus number usage for a device instance.
old-location: devinst\busnumber_des.htm
old-project: devinst
ms.assetid: 3007e271-fe78-404c-ba97-ceb0be334592
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PBUSNUMBER_DES, BUSNUMBER_DES, BUSNUMBER_DES structure [Device and Driver Installation], BusNumber_Des_s, PBUSNUMBER_DES, PBUSNUMBER_DES structure pointer [Device and Driver Installation], cfgmgr32/BUSNUMBER_DES, cfgmgr32/PBUSNUMBER_DES, cfgmgrst_791be216-3ef2-407b-b250-4e09f40356a3.xml, devinst.busnumber_des"
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
req.typenames: BUSNUMBER_DES, *PBUSNUMBER_DES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - cfgmgr32.h
api_name:
 - BUSNUMBER_DES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# BusNumber_Des_s structure


## -description


The BUSNUMBER_DES structure is used for specifying either a resource list or a resource requirements list that describes bus number usage for a device instance. For more information about resource lists and resource requirements lists, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff547012">Hardware Resources</a>.


## -struct-fields




### -field BUSD_Count





#### For a resource list:

Zero.



#### For a resource requirements list:

The number of elements in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff537831">BUSNUMBER_RANGE</a> array that is included in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff537838">BUSNUMBER_RESOURCE</a> structure.


### -field BUSD_Type

Must be set to the constant value <b>BusNumberType_Range</b>.


### -field BUSD_Flags

<i>Not used.</i>


### -field BUSD_Alloc_Base





#### For a resource list:

The lowest-numbered of a range of contiguous bus numbers allocated to the device.



#### For a resource requirements list:

Zero.


### -field BUSD_Alloc_End





#### For a resource list:

The highest-numbered of a range of contiguous bus numbers allocated to the device.



#### For a resource requirements list:

Zero.


## -remarks



The BUSNUMBER_DES structure is included as a member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff537838">BUSNUMBER_RESOURCE</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff537831">BUSNUMBER_RANGE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff537838">BUSNUMBER_RESOURCE</a>
 

 

