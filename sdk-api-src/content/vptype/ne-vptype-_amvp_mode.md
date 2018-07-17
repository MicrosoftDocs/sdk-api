---
UID: NE:vptype._AMVP_MODE
title: "_AMVP_MODE"
author: windows-sdk-content
description: Specifies the various modes for video ports.
old-location: dshow\amvp_mode.htm
old-project: DirectShow
ms.assetid: 73d63ca2-17fb-4e27-9ea5-62686117254a
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: AMVP_MODE, AMVP_MODE , AMVP_MODE enumeration [DirectShow], AMVP_MODEEnumeration, AMVP_MODE_BOBINTERLEAVED, AMVP_MODE_SKIPEVEN, AMVP_MODE_SKIPODD, AMVP_MODE_WEAVE, MODE_BOBNONINTERLEAVED, _AMVP_MODE, dshow.amvp_mode, vptype/AMVP_MODE, vptype/AMVP_MODE_BOBINTERLEAVED, vptype/AMVP_MODE_SKIPEVEN, vptype/AMVP_MODE_SKIPODD, vptype/AMVP_MODE_WEAVE, vptype/MODE_BOBNONINTERLEAVED
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: vptype.h
req.include-header: 
req.target-type: Windows
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
req.typenames: AMVP_MODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - vptype.h
api_name:
 - AMVP_MODE
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# _AMVP_MODE enumeration


## -description



Specifies the various modes for video ports.




## -enum-fields




### -field AMVP_MODE_WEAVE


            
              Weave.
          


### -field AMVP_MODE_BOBINTERLEAVED


            Interleaved bob. Bob mode in which resources are allocated to switch to weave mode, for example, on the next frame.
          


### -field AMVP_MODE_BOBNONINTERLEAVED


### -field AMVP_MODE_SKIPEVEN


            Skip even fields.
          


### -field AMVP_MODE_SKIPODD


            Skip odd fields.
          


#### - MODE_BOBNONINTERLEAVED


            Noninterleaved bob. Bob mode in which resources are not allocated to switch to weave mode.
          


## -see-also




<b></b>



<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>
 

 

