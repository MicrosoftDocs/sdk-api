---
UID: NF:winspool.AddPrintProvidorW
title: AddPrintProvidorW function
author: windows-driver-content
description: The AddPrintProvidor function installs a local print provider and links the configuration, data, and provider files.
old-location: gdi\addprintprovidor.htm
old-project: printdocs
ms.assetid: f34549c3-0474-48ba-9307-5b36f02dbe1c
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: 1, 2, AddPrintProvidor, AddPrintProvidor function [Windows GDI], AddPrintProvidorA, AddPrintProvidorW, _win32_AddPrintProvidor, gdi.addprintprovidor, winspool/AddPrintProvidor, winspool/AddPrintProvidorA, winspool/AddPrintProvidorW
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
req.unicode-ansi: AddPrintProvidorW (Unicode) and AddPrintProvidorA (ANSI)
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
-	AddPrintProvidor
-	AddPrintProvidorA
-	AddPrintProvidorW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# AddPrintProvidorW function


## -description


The <b>AddPrintProvidor</b> function installs a local print provider and links the configuration, data, and provider files.


## -parameters




### -param pName [in]

A pointer to a null-terminated string that specifies the name of the server on which the provider should be installed. For systems that only support local installation of providers, this parameter should be <b>NULL</b>.


### -param Level [in]

The level of the structure to which <i>pProviderInfo</i> points. It can be one of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Function uses a <a href="https://msdn.microsoft.com/0eff115a-b3d2-4c8f-b820-46e7f62dd295">PROVIDOR_INFO_1</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">

                 Function uses a <a href="https://msdn.microsoft.com/840523ca-22d0-460f-81fb-e0a9e2d4f5d6">PROVIDOR_INFO_2</a> structure.

</td>
</tr>
</table>
 


### -param pProvidorInfo

TBD




#### - pProviderInfo [in]

A pointer to a print provider structure, as indicated by <i>Level</i>.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
Before an application calls the <b>AddPrintProvidor</b> function, all files required by the provider must be copied to the SYSTEM32 directory.

A provider added by <b>AddPrintProvidor</b> may be removed by calling <a href="https://msdn.microsoft.com/b7104f9a-111c-4904-a355-063bb4cc81f1">DeletePrintProvidor</a>.




## -see-also




<a href="https://msdn.microsoft.com/b7104f9a-111c-4904-a355-063bb4cc81f1">DeletePrintProvidor</a>



<a href="https://msdn.microsoft.com/0eff115a-b3d2-4c8f-b820-46e7f62dd295">PROVIDOR_INFO_1</a>



<a href="https://msdn.microsoft.com/840523ca-22d0-460f-81fb-e0a9e2d4f5d6">PROVIDOR_INFO_2</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

