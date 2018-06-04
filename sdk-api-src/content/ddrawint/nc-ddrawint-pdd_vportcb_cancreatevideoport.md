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

# PDD_VPORTCB_CANCREATEVIDEOPORT callback function


## -description


The <i>DdVideoPortCanCreate</i> callback function determines whether the driver can support a DirectDraw VPE object of the specified description.


## -parameters




### -param Arg1








#### - lpCanCreateVideoPort

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550509">DD_CANCREATEVPORTDATA</a> structure that contains the information necessary for the driver to determine whether the specified DirectDraw VPE object can be supported.


## -returns



<i>DdVideoPortCanCreate</i> returns one of the following callback codes:




## -remarks



<i>DdVideoPortCanCreate</i> must be implemented in drivers that support VPE.

The driver should check the members of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550402">DDVIDEOPORTDESC</a> structure to which the <b>lpDDVideoPortDesc</b> member of the DD_CANCREATEVPORTDATA structure at <i>lpCanCreateVideoPort</i> points to determine whether the hardware supports the specified type of VPE object.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550402">DDVIDEOPORTDESC</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550509">DD_CANCREATEVPORTDATA</a>



<a href="https://msdn.microsoft.com/eeaf3cda-6220-4e8e-8f9e-9f52d1b05ab7">DdVideoPortCreate</a>
 

 

