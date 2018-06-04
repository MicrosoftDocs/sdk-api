---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _PSFEATURE_OUTPUT structure


## -description



The <b>PSFEATURE_OUTPUT</b> structure contains information about PostScript driver output options. This structure is used with the <a href="https://msdn.microsoft.com/0824b854-a4ed-4e09-a665-b7ec3dd99671">GET_PS_FEATURESETTING</a> printer escape function.




## -struct-fields




### -field bPageIndependent

<b>TRUE</b> if PostScript output is page-independent or <b>FALSE</b> if PostScript output is page-dependent.


### -field bSetPageDevice

<b>TRUE</b> if printer feature code (setpagedevice's) is included or <b>FALSE</b> if all printer feature code is suppressed.


## -see-also




<a href="https://msdn.microsoft.com/0824b854-a4ed-4e09-a665-b7ec3dd99671">GET_PS_FEATURESETTING</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

