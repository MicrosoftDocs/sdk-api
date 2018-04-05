---
UID: NC:fwpmu.FWPM_SYSTEM_PORTS_CALLBACK0
title: FWPM_SYSTEM_PORTS_CALLBACK0
author: windows-driver-content
description: Is used to add custom behavior to the system port subscription process.
old-location: fwp\fwpm_system_ports_callback0_func.htm
old-project: FWP
ms.assetid: 91bf0d89-f760-4de9-8e9b-ece93b6c84ae
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: FWPM_SYSTEM_PORTS_CALLBACK0, FWPM_SYSTEM_PORTS_CALLBACK0 function pointer [Filtering], fwp.fwpm_system_ports_callback0_func, fwpmu/FWPM_SYSTEM_PORTS_CALLBACK0
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FWPM_VSWITCH_EVENT_SUBSCRIPTION0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Fwpmu.h
api_name:
-	FWPM_SYSTEM_PORTS_CALLBACK0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FWPM_SYSTEM_PORTS_CALLBACK0 callback


## -description


The <b>FWPM_SYSTEM_PORTS_CALLBACK0</b> function is used to add custom behavior to the system port subscription process.


## -parameters




### -param *context [in, out]

Type: <b>void*</b>

Optional context pointer. It contains the value of the <i>context</i> parameter of the <a href="https://msdn.microsoft.com/e0eecf0e-e6b2-4df9-8a8e-766ee5c8189f">FwpmSystemPortsSubscribe0</a> function.


### -param *sysPorts [in]

Type: <b>const <a href="https://msdn.microsoft.com/cf6fbd43-f603-417d-925d-418d9aec5a03">FWPM_SYSTEM_PORTS0</a>*</b>

The system port information.


## -returns



This function pointer does not return a value.




## -remarks



Call <a href="https://msdn.microsoft.com/e0eecf0e-e6b2-4df9-8a8e-766ee5c8189f">FwpmSystemPortsSubscribe0</a> to register this callback function.

<b>FWPM_SYSTEM_PORTS_CALLBACK0</b> is a specific implementation of FWPM_SYSTEM_PORTS_CALLBACK. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/cf6fbd43-f603-417d-925d-418d9aec5a03">FWPM_SYSTEM_PORTS0</a>



<a href="https://msdn.microsoft.com/e0eecf0e-e6b2-4df9-8a8e-766ee5c8189f">FwpmSystemPortsSubscribe0</a>
 

 

