---
UID: NF:wiautil.wiauDbgLegacyTrace2
title: wiauDbgLegacyTrace2 function
author: windows-driver-content
description: The wiauDbgLegacyTrace2 function logs a trace message.
old-location: image\wiaudbglegacytrace2.htm
old-project: image
ms.assetid: 911a7089-d4ac-4da0-8be6-a3a36567635c
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiaudbglegacytrace2, wiauDbgLegacyTrace2, wiauDbgLegacyTrace2 function [Imaging Devices], wiauFncs_8fbdcd6b-cb2b-461b-81f0-880675d0124b.xml, wiautil/wiauDbgLegacyTrace2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wiautil.h
req.include-header: Wiautil.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows XP and later.
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
req.typenames: SKIP_AMOUNT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wiautil.h
api_name:
-	wiauDbgLegacyTrace2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# wiauDbgLegacyTrace2 function


## -description


The <b>wiauDbgLegacyTrace2</b> function logs a trace message.


## -parameters




### -param hInstance

Specifies the handle to the DLL instance.


### -param fmt

TBD


### -param param

TBD




####### - fmt, ...

Pointer to a format string that specifies a variable argument list, which starts with an ANSI format string containing the message and any conversion specifiers. The ellipsis (...) specifies a variable number of arguments that are to be output.


## -returns



None




## -remarks



The <b>wiauDbgLegacyTrace2</b> function is identical to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550161">wiauDbgTrace</a> function except that the former has a parameter that specifies the handle to the DLL instance and the latter has a parameter used to identify the function or method that is active when the function is called.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550161">wiauDbgTrace</a>
 

 

