---
UID: NC:ddrawint.PDD_PALCB_SETENTRIES
title: PDD_PALCB_SETENTRIES
author: windows-driver-content
description: The DdSetEntries callback function updates the palette entries in the specified palette.
old-location: display\ddsetentries.htm
old-project: display
ms.assetid: 41b0b433-288d-4d7b-b961-2789b2540761
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: DdSetEntries, DdSetEntries callback function [Display Devices], PDD_PALCB_SETENTRIES, ddfncs_904cb314-1d34-4ace-b1ba-92e25ed8f293.xml, ddrawint/DdSetEntries, display.ddsetentries
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
-	DdSetEntries
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PDD_PALCB_SETENTRIES callback


## -description


The <i>DdSetEntries</i> callback function updates the palette entries in the specified palette. 


## -parameters




### -param Arg1








#### - lpSetEntries

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551700">DD_SETENTRIESDATA</a> structure that contains the information required to set the palette's entries.


## -returns



<i>DdSetEntries</i> returns one of the following callback codes:




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551700">DD_SETENTRIESDATA</a>
 

 

