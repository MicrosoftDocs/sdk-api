---
UID: NF:wingdi.EndDoc
title: EndDoc function
author: windows-sdk-content
description: The EndDoc function ends a print job.
old-location: gdi\enddoc.htm
old-project: printdocs
ms.assetid: bf63ea0f-cc73-4943-9c84-52b3b77e141c
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: EndDoc, EndDoc function [Windows GDI], _win32_EndDoc, gdi.enddoc, wingdi/EndDoc
ms.prod: windows
ms.technology: windows-sdk
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
-	Ext-MS-Win-GDI-print-l1-1-0.dll
-	GDI32Full.dll
api_name:
-	EndDoc
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# EndDoc function


## -description


The <b>EndDoc</b> function ends a print job.


## -parameters




### -param hdc [in]

Handle to the device context for the print job.


## -returns



If the function succeeds, the return value is greater than zero.

If the function fails, the return value is less than or equal to zero.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
Applications should call <b>EndDoc</b> immediately after finishing a print job.


#### Examples

For a sample program that uses this function, see <a href="https://msdn.microsoft.com/C212DD92-2B90-45BC-8746-29C193FBDF69">How To: Print Using the GDI Print API</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/53143463-b9fc-4378-aea9-da6c73a7cd03">StartDoc</a>
 

 

