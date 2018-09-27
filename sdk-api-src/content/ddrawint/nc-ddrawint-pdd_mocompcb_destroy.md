---
UID: NC:ddrawint.PDD_MOCOMPCB_DESTROY
title: PDD_MOCOMPCB_DESTROY
author: windows-sdk-content
description: The DdMoCompDestroy callback function notifies the driver that this motion compensation object will no longer be used. The driver now needs to perform any necessary cleanup.
old-location: display\ddmocompdestroy.htm
tech.root: display
ms.assetid: 7a8900d0-4c9f-4600-8408-197f4e7c78ba
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: DdMoCompDestroy, DdMoCompDestroy callback function [Display Devices], PDD_MOCOMPCB_DESTROY, PDD_MOCOMPCB_DESTROY callback, ddfncs_7fbf03ee-a58a-40f0-88b6-f9bf68cb3f8f.xml, ddrawint/DdMoCompDestroy, display.ddmocompdestroy
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ddrawint.h
api_name:
 - DdMoCompDestroy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDD_MOCOMPCB_DESTROY callback function


## -description


The <b>DdMoCompDestroy</b> callback function notifies the driver that this motion compensation object will no longer be used. The driver now needs to perform any necessary cleanup.


## -parameters




### -param Arg1








#### - lpDestroyData

Points to a <a href="https://msdn.microsoft.com/0db32ded-2e32-471d-a752-1f5beffec684">DD_DESTROYMOCOMPDATA</a> structure that contains the information needed to finish motion compensation.


## -returns



<b>DdMoCompDestroy</b> returns one of the following callback codes:




## -remarks



<b>DdMoCompDestroy</b> can be optionally implemented in DirectDraw drivers. It is not required for motion compensation support.




## -see-also




<a href="https://msdn.microsoft.com/0db32ded-2e32-471d-a752-1f5beffec684">DD_DESTROYMOCOMPDATA</a>
 

 

