---
UID: NF:wingdi.EndPage
title: EndPage function
author: windows-driver-content
description: The EndPage function notifies the device that the application has finished writing to a page. This function is typically used to direct the device driver to advance to a new page.
old-location: gdi\endpage.htm
old-project: printdocs
ms.assetid: 33e6d005-f00d-4b87-bf7c-fc79c1d05514
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: EndPage, EndPage function [Windows GDI], _win32_EndPage, gdi.endpage, wingdi/EndPage
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
req.typenames: FAX_TIME, *PFAX_TIME
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
-	EndPage
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# EndPage function


## -description


The <b>EndPage</b> function notifies the device that the application has finished writing to a page. This function is typically used to direct the device driver to advance to a new page.


## -parameters




### -param hdc [in]

A handle to the device context for the print job.


## -returns



If the function succeeds, the return value is greater than zero.

If the function fails, the return value is less than or equal to zero.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
Use the <a href="https://msdn.microsoft.com/3f77db51-90d1-4a87-812b-1e129ae8fde9">ResetDC</a> function to change the device mode, if necessary, after calling the <b>EndPage</b> function. Note that a call to <b>ResetDC</b> resets all device context attributes back to default values. Neither <b>EndPage</b> nor <a href="https://msdn.microsoft.com/library/windows/hardware/dn923219">StartPage</a> resets the device context attributes. Device context attributes remain constant across subsequent pages. You do not need to re-select objects and set up the mapping mode again before printing the next page; however, doing so will produce the same results and reduce code differences between versions of Windows.


         When a page in a spooled file exceeds approximately 350 MB, it may fail to print and not send an error message. For example, this can occur when printing large EMF files. The page size limit depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.


#### Examples

For a sample program that uses this function, see <a href="https://msdn.microsoft.com/C212DD92-2B90-45BC-8746-29C193FBDF69">How To: Print Using the GDI Print API</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/3f77db51-90d1-4a87-812b-1e129ae8fde9">ResetDC</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn923219">StartPage</a>
 

 

