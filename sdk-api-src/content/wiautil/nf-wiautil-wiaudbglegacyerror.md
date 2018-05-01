---
UID: NF:wiautil.wiauDbgLegacyError
title: wiauDbgLegacyError function
author: windows-driver-content
description: The wiauDbgLegacyError function logs an error message.
old-location: image\wiaudbglegacyerror.htm
old-project: image
ms.assetid: c2a9bd35-ce3a-4640-9982-b470e98b4692
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiaudbglegacyerror, wiauDbgLegacyError, wiauDbgLegacyError function [Imaging Devices], wiauFncs_03e81269-0a09-42c4-8d0d-1f808e6ef69e.xml, wiautil/wiauDbgLegacyError
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
-	wiauDbgLegacyError
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# wiauDbgLegacyError function


## -description


The <b>wiauDbgLegacyError</b> function logs an error message.


## -parameters




### -param fmt

TBD


### -param param

TBD




####### - fmt, ...

Pointer to a format string that specifies a variable argument list, which starts with an ANSI format string containing the message and any conversion specifiers. The ellipsis (...) specifies a variable number of arguments that are to be output.


## -returns



None




## -remarks



The <b>wiauDbgLegacyError</b> function is identical to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff549633">wiauDbgError</a> function except that the latter function has an additional parameter used to identify the function or method that is active when the function is called.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549633">wiauDbgError</a>
 

 

