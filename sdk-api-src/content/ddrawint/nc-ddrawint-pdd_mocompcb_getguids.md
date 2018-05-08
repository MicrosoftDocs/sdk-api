---
UID: NC:ddrawint.PDD_MOCOMPCB_GETGUIDS
title: PDD_MOCOMPCB_GETGUIDS
author: windows-driver-content
description: The DdMoCompGetGuids callback function retrieves the number of GUIDs the driver supports.
old-location: display\ddmocompgetguids.htm
old-project: display
ms.assetid: 22c6a3f2-4a27-4a4b-a021-8f2be04e4f87
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: DdMoCompGetGuids, DdMoCompGetGuids callback function [Display Devices], PDD_MOCOMPCB_GETGUIDS, PDD_MOCOMPCB_GETGUIDS callback, ddfncs_224ee005-4c85-41cc-afcf-2958c31dfd45.xml, ddrawint/DdMoCompGetGuids, display.ddmocompgetguids
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: ddrawint.h
req.include-header: Winddi.h
req.target-type: Desktop
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
req.typenames: "*LPDDHAL_DESTROYDDLOCALDATA, DDHAL_DESTROYDDLOCALDATA"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ddrawint.h
api_name:
-	DdMoCompGetGuids
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PDD_MOCOMPCB_GETGUIDS callback function


## -description


The <b>DdMoCompGetGuids</b> callback function retrieves the number of GUIDs the driver supports.


## -parameters




### -param Arg1








#### - lpGetGuidData

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551587">DD_GETMOCOMPGUIDSDATA</a> structure that contains the GUID information.


## -returns



<b>DdMoCompGetGuids</b> returns one of the following callback codes:




## -remarks



DirectDraw drivers that support motion compensation must implement <b>DdMoCompGetGuids</b>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551587">DD_GETMOCOMPGUIDSDATA</a>
 

 

