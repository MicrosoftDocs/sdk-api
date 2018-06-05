---
UID: NC:ddrawint.PDD_SURFCB_GETFLIPSTATUS
title: PDD_SURFCB_GETFLIPSTATUS
author: windows-sdk-content
description: The DdGetFlipStatus callback function determines whether the most recently requested flip on a surface has occurred.
old-location: display\ddgetflipstatus.htm
old-project: display
ms.assetid: ec556891-e091-4c52-a155-cb6ba8011f71
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: DdGetFlipStatus, DdGetFlipStatus callback function [Display Devices], PDD_SURFCB_GETFLIPSTATUS, PDD_SURFCB_GETFLIPSTATUS callback, ddfncs_129ef755-b85d-4f99-b62b-87124364c283.xml, ddrawint/DdGetFlipStatus, display.ddgetflipstatus
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: "*LPDDHAL_DESTROYDDLOCALDATA, DDHAL_DESTROYDDLOCALDATA"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ddrawint.h
api_name:
-	DdGetFlipStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PDD_SURFCB_GETFLIPSTATUS callback function


## -description


The <b>DdGetFlipStatus</b> callback function determines whether the most recently requested flip on a surface has occurred.


## -parameters




### -param Arg1








#### - lpGetFlipStatus

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551564">DD_GETFLIPSTATUSDATA</a> structure that contains the information required to perform the flip status query.


## -returns



<b>DdGetFlipStatus</b> returns one of the following callback codes:




## -remarks



The driver should report its flip status based on the flag set in the <b>dwFlags</b> member of the structure that <b>lpGetFlipStatus</b> points to as follows:

<ul>
<li>
If the flag is DDGFS_CANFLIP, the driver should determine whether the surface is currently involved in a flip. If a flip or a blit is not in progress and if the hardware is otherwise capable of currently accepting a flip request, the driver should return DD_OK in <b>ddRVal</b>. If a flip is in progress or if the hardware cannot currently accept a flip request, the driver should set <b>ddRVal</b> to DDERR_WASSTILLDRAWING.

</li>
<li>
If the flag is DDGFS_ISFLIPDONE, the driver should set <b>ddRVal</b> to DDERR_WASSTILLDRAWING if a flip is currently in progress; otherwise it should return DD_OK.

</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551564">DD_GETFLIPSTATUSDATA</a>
 

 

