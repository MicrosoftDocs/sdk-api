---
UID: NF:winspool.DeletePrintProvidorA
title: DeletePrintProvidorA function
author: windows-driver-content
description: The DeletePrintProvidor function removes a print provider added by the AddPrintProvidor function.
old-location: gdi\deleteprintprovidor.htm
old-project: printdocs
ms.assetid: b7104f9a-111c-4904-a355-063bb4cc81f1
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: DeletePrintProvidor, DeletePrintProvidor function [Windows GDI], DeletePrintProvidorA, DeletePrintProvidorW, _win32_DeletePrintProvidor, gdi.deleteprintprovidor, winspool/DeletePrintProvidor, winspool/DeletePrintProvidorA, winspool/DeletePrintProvidorW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winspool.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DeletePrintProvidorW (Unicode) and DeletePrintProvidorA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRINT_EXECUTION_CONTEXT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Winspool.drv
api_name:
-	DeletePrintProvidor
-	DeletePrintProvidorA
-	DeletePrintProvidorW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# DeletePrintProvidorA function


## -description


The <b>DeletePrintProvidor</b> function removes a print provider added by the <a href="https://msdn.microsoft.com/f34549c3-0474-48ba-9307-5b36f02dbe1c">AddPrintProvidor</a> function.


## -parameters




### -param pName [in]

Reserved; must be <b>NULL</b>.


### -param pEnvironment [in]

A pointer to a null-terminated string that specifies the environment from which the provider is to be removed (for example, Windows NT x86, Windows IA64, or Windows x64). If this parameter is <b>NULL</b>, the provider is removed from the current environment of the calling application and client machine (not of the destination application and print server). <b>NULL</b> is the recommended value because it provides maximum portability.


### -param pPrintProvidorName

TBD




#### - pPrintProviderName [in]

A pointer to a null-terminated string that specifies the name of the provider to be removed.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/f34549c3-0474-48ba-9307-5b36f02dbe1c">AddPrintProvidor</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

