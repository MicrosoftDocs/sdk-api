---
UID: NC:ddrawint.PDD_MOCOMPCB_ENDFRAME
title: PDD_MOCOMPCB_ENDFRAME
author: windows-sdk-content
description: The DdMoCompEndFrame callback function completes a decoded frame.
old-location: display\ddmocompendframe.htm
old-project: display
ms.assetid: 3589f003-32fc-44c4-867a-abf54f347de9
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: DdMoCompEndFrame, DdMoCompEndFrame callback function [Display Devices], PDD_MOCOMPCB_ENDFRAME, PDD_MOCOMPCB_ENDFRAME callback, ddfncs_24cad2ef-0770-46d5-a3f3-a4565ec66626.xml, ddrawint/DdMoCompEndFrame, display.ddmocompendframe
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
-	DdMoCompEndFrame
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PDD_MOCOMPCB_ENDFRAME callback function


## -description


The <b>DdMoCompEndFrame</b> callback function completes a decoded frame.


## -parameters




### -param Arg1








#### - lpFrameData

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551517">DD_ENDMOCOMPFRAMEDATA</a> structure that contains the information needed to complete the decoded frame.


## -returns



<b>DdMoCompEndFrame</b> returns one of the following callback codes:




## -remarks



DirectDraw drivers that support motion compensation must implement <b>DdMoCompEndFrame</b>.

DirectDraw ensures that begin and end frames will be properly paired.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551517">DD_ENDMOCOMPFRAMEDATA</a>
 

 

