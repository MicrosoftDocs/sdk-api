---
UID: NF:wiautil.wiauDbgLegacyHresult2
title: wiauDbgLegacyHresult2 function
author: windows-driver-content
description: The wiauDbgLegacyHresult2 function logs a default message containing an HRESULT.
old-location: image\wiaudbglegacyhresult2.htm
old-project: image
ms.assetid: 1b73c94b-07a8-4b65-8ed7-d5f1a073c3b2
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiaudbglegacyhresult2, wiauDbgLegacyHresult2, wiauDbgLegacyHresult2 function [Imaging Devices], wiauFncs_b980cd55-047b-4870-9bad-928253d0ce77.xml, wiautil/wiauDbgLegacyHresult2
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
-	wiautil.h
api_name:
-	wiauDbgLegacyHresult2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# wiauDbgLegacyHresult2 function


## -description


The <b>wiauDbgLegacyHresult2</b> function logs a default message containing an HRESULT.


## -parameters




### -param hInstance [in]

Specifies the handle to the DLL instance.


### -param hr

Specifies the HRESULT to be logged.


## -returns



None




## -remarks



A call to the <b>wiauDbgLegacyHresult2</b> function is equivalent to the following call to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff549637">wiauDbgErrorHr</a> function:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>wiauDbgErrorHr(hr, "", "");</pre>
</td>
</tr>
</table></span></div>
That is, only one line is output to the log file and/or debugger. The line has the following form:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>ERROR HRESULT = HRESULT value, Error text for HRESULT </pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549637">wiauDbgErrorHr</a>
 

 

