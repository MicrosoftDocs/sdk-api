---
UID: NC:routprot.PSTART_COMPLETE
title: PSTART_COMPLETE
author: windows-driver-content
description: Router Manager calls the StartComplete function to inform the routing protocol that initialization is complete and all interfaces have been added. The routing protocol should wait for this call before starting any protocol-specific behavior.
old-location: rras\startcomplete.htm
old-project: RRAS
ms.assetid: 1dace3a7-8e97-405c-b1fe-f5a67c05fb0c
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: PSTART_COMPLETE, PSTART_COMPLETE callback, StartComplete, StartComplete callback function [RAS], _mpr_startcomplete, routprot/StartComplete, rras.startcomplete
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: routprot.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Routprot.h
api_name:
-	StartComplete
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PSTART_COMPLETE callback function


## -description


Router Manager calls the 
<b>StartComplete</b> function to inform the routing protocol that initialization is complete and all interfaces have been added. The routing protocol should wait for this call before starting any protocol-specific behavior.

The <a href="https://msdn.microsoft.com/7046c4c2-b0bd-4459-b361-e46ce876823f">PSTART_COMPLETE</a> type defines a pointer to this callback function. <i>StartComplete</i> is a placeholder for the application-defined function name.


## -parameters




### -param Arg1








## -returns



This function should return NO_ERROR.




## -see-also




<a href="https://msdn.microsoft.com/8c1c0173-5abf-4e44-a633-16742fd2a4c0">StartProtocol</a>
 

 

