---
UID: NF:wiautil.wiauDbgError
title: wiauDbgError function
author: windows-driver-content
description: The wiauDbgError function logs an error message.
old-location: image\wiaudbgerror.htm
old-project: image
ms.assetid: 112d6f90-33b3-446b-943c-8995e6ec3378
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiaudbgerror, wiauDbgError, wiauDbgError function [Imaging Devices], wiauFncs_73184286-df53-4272-9fa8-aae1d1fb3dbc.xml, wiautil/wiauDbgError
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
-	wiauDbgError
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# wiauDbgError function


## -description


The <b>wiauDbgError</b> function logs an error message.


## -parameters




### -param fname

Pointer to a string containing the name of the function or method into which the call to <b>wiauDbgDump</b> is inserted.


### -param fmt

TBD


### -param param

TBD




####### - fmt, ...

Pointer to a format string that specifies a variable argument list, which starts with an ANSI format string containing the message and any conversion specifiers. The ellipsis (...) specifies a variable number of arguments that are to be output. 


## -returns



None




## -remarks



The <b>wiauDbgError</b> typically is used to display an error message with no data, such as in the following example:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>wiauDbgError("Read", "Attempting to read past end of buffer");</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549627">wiauDbgDump</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549637">wiauDbgErrorHr</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550161">wiauDbgTrace</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550163">wiauDbgWarning</a>
 

 

