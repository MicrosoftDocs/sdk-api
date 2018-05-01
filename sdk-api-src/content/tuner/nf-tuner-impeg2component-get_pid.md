---
UID: NF:tuner.IMPEG2Component.get_PID
title: IMPEG2Component::get_PID method
author: windows-driver-content
description: The get_PID method returns the packet identifier (PID) for this substream.
old-location: mstv\impeg2component_get_pid.htm
old-project: mstv
ms.assetid: 7d6b0b2f-fe48-4fc5-bb3b-639bb8ee2df8
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IMPEG2Component, IMPEG2Component interface [Microsoft TV Technologies], get_PID method, IMPEG2Component::get_PID, IMPEG2Componentget_PID, get_PID method [Microsoft TV Technologies], get_PID method [Microsoft TV Technologies], IMPEG2Component interface, get_PID,IMPEG2Component.get_PID, mstv.impeg2component_get_pid, tuner/IMPEG2Component::get_PID
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IMPEG2Component.get_PID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IMPEG2Component::get_PID method


## -description



The <b>get_PID</b> method returns the packet identifier (PID) for this substream.




## -parameters




### -param PID






#### - pPID [out]

Pointer to a variable that receives the PID.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/63d1ae17-8e38-457e-98d7-e81e7576f1c1">IMPEG2Component Interface</a>
 

 

