---
UID: NF:wingdi.Escape
title: Escape function
author: windows-driver-content
description: Enables an application to access the system-defined device capabilities that are not available through GDI.
old-location: gdi\escape.htm
old-project: printdocs
ms.assetid: ba21b680-78a8-45a2-94e1-01b377b74787
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: Escape, Escape function [Windows GDI], _win32_Escape_v3, gdi.escape, wingdi/Escape
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	gdi32.dll
-	Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
api_name:
-	Escape
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# Escape function


## -description


The <b>Escape</b> function enables an application to access the system-defined device capabilities that are not available through GDI. Escape calls made by an application are translated and sent to the driver.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param iEscape

TBD


### -param cjIn

TBD


### -param pvIn

TBD


### -param pvOut

TBD




#### - cbInput [in]

The number of bytes of data pointed to by the <i>lpvInData</i> parameter. This can be 0.


#### - lpvInData [in]

A pointer to the input structure required for the specified escape.


#### - lpvOutData [out]

A pointer to the structure that receives output from this escape. This parameter should be <b>NULL</b> if no data is returned.


#### - nEscape [in]

The escape function to be performed. This parameter must be one of the predefined escape values listed in Remarks. Use the <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a> function if your application defines a private escape value.


## -returns



If the function succeeds, the return value is greater than zero, except with the <a href="https://msdn.microsoft.com/25aaf9da-50ec-4fde-af93-aa2c03a74d6d">QUERYESCSUPPORT</a> printer escape, which checks for implementation only. If the escape is not implemented, the return value is zero.

If the function fails, the return value is a system error code.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The effect of passing 0 for <i>cbInput</i> will depend on the value of <i>nEscape</i> and on the driver that is handling the escape.

Of the original printer escapes, only the following can be used.

<table>
<tr>
<th>Escape</th>
<th>Description</th>
</tr>
<tr>
<td>
QUERYESCSUPPORT

</td>
<td>
Determines whether a particular escape is implemented by the device driver.

</td>
</tr>
<tr>
<td>
PASSTHROUGH

</td>
<td>
Allows the application to send data directly to a printer.

</td>
</tr>
</table>
 

Use the <a href="https://msdn.microsoft.com/library/windows/hardware/dn923219">StartPage</a> function to prepare the printer driver to receive data.




## -see-also




<a href="https://msdn.microsoft.com/4ecc371c-34fa-4073-96fe-0de03b84d7e3">AbortDoc</a>



<a href="https://msdn.microsoft.com/e89a2f6f-2bac-4369-b526-f8e15028698b">DocumentProperties</a>



<a href="https://msdn.microsoft.com/bf63ea0f-cc73-4943-9c84-52b3b77e141c">EndDoc</a>



<a href="https://msdn.microsoft.com/33e6d005-f00d-4b87-bf7c-fc79c1d05514">EndPage</a>



<a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a>



<a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/1d4c961b-178b-47af-b983-5b7327919f93">PrinterProperties</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/3f77db51-90d1-4a87-812b-1e129ae8fde9">ResetDC</a>



<a href="https://msdn.microsoft.com/5b6333fc-f1c3-4c76-906c-0fd13bb73953">SetAbortProc</a>



<a href="https://msdn.microsoft.com/53143463-b9fc-4378-aea9-da6c73a7cd03">StartDoc</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn923219">StartPage</a>
 

 

