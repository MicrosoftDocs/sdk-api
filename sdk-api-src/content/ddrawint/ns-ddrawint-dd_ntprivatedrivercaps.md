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

# DD_NTPRIVATEDRIVERCAPS structure


## -description


The DD_NTPRIVATEDRIVERCAPS structure enables the driver to change the behavior of Microsoft DirectDraw when DirectDraw is creating surfaces.


## -struct-fields




### -field dwSize

Specifies the size in bytes of this DD_NTPRIVATEDRIVERCAPS structure.


### -field dwPrivateCaps

Indicates how DirectDraw should create the surface.





#### DDHAL_PRIVATECAP_AUTOMICSURFACECREATION

When this flag is set, it indicates that the driver requests <a href="https://msdn.microsoft.com/45c793ed-34e8-4a15-91f4-9a258c1842fd">DdCreateSurface</a> to be called only once when the application creates a complex flipping chain using a single <b>CreateSurface</b> call. In this case, the <b>lplpSList</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550540">DD_CREATESURFACEDATA</a> structure points to a list of surfaces to create (rather than a single surface) and <b>dwSCnt</b> contains the number of surfaces in the list. 



#### DDHAL_PRIVATECAP_NOTIFYPRIMARYCREATION

When this flag is set, the driver's <a href="https://msdn.microsoft.com/45c793ed-34e8-4a15-91f4-9a258c1842fd">DdCreateSurface</a> function is called when creating a primary surface. If this flag is not set, the driver's <i>DdCreateSurface</i> function is not called.


## -remarks



The behavior of DirectDraw emulates the surface creation techniques employed by DirectDraw when creating surfaces for Microsoft Windows 98/Me.

When the DDHAL_PRIVATECAP_AUTOMICSURFACECREATION flag is not set, DirectDraw performs surface creation using the original method, that is, it calls the driver's <a href="https://msdn.microsoft.com/45c793ed-34e8-4a15-91f4-9a258c1842fd">DdCreateSurface</a> function once for each surface being created.

When the DDHAL_PRIVATECAP_NOTIFYPRIMARYCREATION flag is not set, DirectDraw performs primary surface creation using the original method, that is, it does not call the driver when creating a primary surface.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550540">DD_CREATESURFACEDATA</a>



<a href="https://msdn.microsoft.com/45c793ed-34e8-4a15-91f4-9a258c1842fd">DdCreateSurface</a>
 

 

