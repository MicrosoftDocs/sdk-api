---
UID: NC:ddrawint.PDD_SURFCB_SETCOLORKEY
title: PDD_SURFCB_SETCOLORKEY
author: windows-sdk-content
description: The DdSetColorKey callback function sets the color key value for the specified surface.
old-location: display\ddsetcolorkey.htm
tech.root: display
ms.assetid: 4b4ee889-15c8-4a7c-a9d8-adab27b271dd
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: DdSetColorKey, DdSetColorKey callback function [Display Devices], PDD_SURFCB_SETCOLORKEY, PDD_SURFCB_SETCOLORKEY callback, ddfncs_d15b9bba-6ff4-441e-8bbe-f23e85de8e32.xml, ddrawint/DdSetColorKey, display.ddsetcolorkey
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
 - DdSetColorKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDD_SURFCB_SETCOLORKEY callback function


## -description


The <i>DdSetColorKey</i> callback function sets the color key value for the specified surface. 


## -parameters




### -param Arg1








#### - lpSetColorKey

Points to a <a href="https://msdn.microsoft.com/08d17ac7-a5d4-47ed-9ee4-896471b46769">DD_SETCOLORKEYDATA</a> structure that contains the information required to set the color key for the specified surface.


## -returns



<i>DdSetColorKey</i> returns one of the following callback codes:




## -remarks



<i>DdSetColorKey</i> sets the source or destination color key for the specified surface. Typically, this callback is implemented only for drivers that support overlays with color key capabilities.




## -see-also




<a href="https://msdn.microsoft.com/08d17ac7-a5d4-47ed-9ee4-896471b46769">DD_SETCOLORKEYDATA</a>
 

 

