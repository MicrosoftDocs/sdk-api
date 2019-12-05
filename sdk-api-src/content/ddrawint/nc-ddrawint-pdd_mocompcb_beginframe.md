---
UID: NC:ddrawint.PDD_MOCOMPCB_BEGINFRAME
title: PDD_MOCOMPCB_BEGINFRAME (ddrawint.h)
description: The DdMoCompBeginFrame callback function starts decoding a new frame.
old-location: display\ddmocompbeginframe.htm
tech.root: display
ms.assetid: 0038aedc-2e4f-4d89-878f-7f6f751015cc
ms.date: 12/05/2018
ms.keywords: DdMoCompBeginFrame, DdMoCompBeginFrame callback function [Display Devices], PDD_MOCOMPCB_BEGINFRAME, PDD_MOCOMPCB_BEGINFRAME callback, ddfncs_5bfa2d81-42a3-4615-be52-605e5e3a2b14.xml, ddrawint/DdMoCompBeginFrame, display.ddmocompbeginframe
ms.topic: callback
f1_keywords:
- ddrawint/DdMoCompBeginFrame
dev_langs:
- c++
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
- DdMoCompBeginFrame
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PDD_MOCOMPCB_BEGINFRAME callback function


## -description


The <b>DdMoCompBeginFrame</b> callback function starts decoding a new frame. 


## -parameters




### -param Arg1








#### - lpFrameData

Points to a <a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/ns-ddrawint-dd_beginmocompframedata">DD_BEGINMOCOMPFRAMEDATA</a> structure that contains the information needed to start decoding a new frame.


## -returns



<b>DdMoCompBeginFrame</b> returns one of the following callback codes:




## -remarks



DirectDraw drivers that support motion compensation must implement <b>DdMoCompBeginFrame</b>.

DirectDraw ensures that begin and end frames will be properly paired.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/ns-ddrawint-dd_beginmocompframedata">DD_BEGINMOCOMPFRAMEDATA</a>
 

 

