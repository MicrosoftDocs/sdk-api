---
UID: NC:ddrawint.PDD_MOCOMPCB_CREATE
title: PDD_MOCOMPCB_CREATE
author: windows-sdk-content
description: The DdMoCompCreate callback function notifies the driver that a software decoder will start using motion compensation with the specified GUID.
old-location: display\ddmocompcreate.htm
tech.root: display
ms.assetid: 9413108b-f9b5-4d1c-83a9-b663a9f444bf
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: DdMoCompCreate, DdMoCompCreate callback function [Display Devices], PDD_MOCOMPCB_CREATE, PDD_MOCOMPCB_CREATE callback, ddfncs_b5650d61-0a79-494a-acd7-231d2e859c30.xml, ddrawint/DdMoCompCreate, display.ddmocompcreate
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
 - DdMoCompCreate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDD_MOCOMPCB_CREATE callback function


## -description


The <i>DdMoCompCreate</i> callback function notifies the driver that a software decoder will start using motion compensation with the specified GUID. 


## -parameters




### -param Arg1








#### - lpCreateData

Points to a <a href="https://msdn.microsoft.com/53b2aa38-b007-4938-8fdb-c3482735ae36">DD_CREATEMOCOMPDATA</a> structure that contains the information required to begin using motion compensation.


## -returns



<i>DdMoCompCreate</i> returns one of the following callback codes:




## -remarks



<i>DdMoCompCreate</i> can be optionally implemented in DirectDraw drivers. It is not required for motion compensation support.

<i>DdMoCompCreate</i> also reports the width, height, and format of the output frame. The driver can fail this call if it cannot support motion compensation with these dimensions.




## -see-also




<a href="https://msdn.microsoft.com/53b2aa38-b007-4938-8fdb-c3482735ae36">DD_CREATEMOCOMPDATA</a>
 

 

