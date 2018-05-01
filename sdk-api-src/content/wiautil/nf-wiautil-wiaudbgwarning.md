---
UID: NF:wiautil.wiauDbgWarning
title: wiauDbgWarning function
author: windows-driver-content
description: The wiauDbgWarning function logs a warning message.
old-location: image\wiaudbgwarning.htm
old-project: image
ms.assetid: f10f1c28-0bfd-44c5-a0aa-9f9227f775d2
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiaudbgwarning, wiauDbgWarning, wiauDbgWarning function [Imaging Devices], wiauFncs_1248626b-0d4f-445c-855c-9ba477cf306c.xml, wiautil/wiauDbgWarning
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
-	wiauDbgWarning
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# wiauDbgWarning function


## -description


The <b>wiauDbgWarning</b> function logs a warning message.


## -parameters




### -param fname

Pointer to a string containing the name of the function or method into which the call to <b>wiauDbgWarning</b> is inserted.


### -param fmt

TBD


### -param param

TBD




####### - fmt, ...

Pointer to a format string that specifies a variable argument list, which starts with an ANSI format string containing the warning message and any conversion specifiers. The ellipsis (...) specifies a variable number of arguments that are to be output.


## -returns



None




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549627">wiauDbgDump</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549633">wiauDbgError</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549637">wiauDbgErrorHr</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550161">wiauDbgTrace</a>
 

 

