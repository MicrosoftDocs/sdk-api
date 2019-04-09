---
UID: NF:prntvpt.PTOpenProviderEx
title: PTOpenProviderEx function (prntvpt.h)
author: windows-sdk-content
description: Opens an instance of a print ticket provider.
old-location: gdi\ptopenproviderex.htm
tech.root: printdocs
ms.assetid: 0e65170b-66f6-4238-bdde-0a0b7108a686
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PTOpenProviderEx, PTOpenProviderEx function [Windows GDI], _win32_PTOpenProviderEx, gdi.ptopenproviderex, prntvpt/PTOpenProviderEx
ms.topic: function
req.header: prntvpt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Prntvpt.lib
req.dll: Prntvpt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - prntvpt.dll
api_name:
 - PTOpenProviderEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PTOpenProviderEx function


## -description


Opens an instance of a print ticket provider.


## -parameters




### -param pszPrinterName [in]

A pointer to the full name of a print queue.


### -param dwMaxVersion

The latest version of the <a href="https://msdn.microsoft.com/98d5f8ec-54bd-4e88-b632-ed427b599cb6">Print Schema</a> that the caller supports.


### -param dwPrefVersion

The version of the Print Schema requested by the caller.


### -param phProvider [out]

A pointer to a handle for the provider.


### -param pUsedVersion [out]

A pointer to the version of the Print Schema that the print ticket provider will use.


## -returns



If the operation succeeds, the return value is S_OK, otherwise the <b>HRESULT</b> contains an error code.

For more information about COM error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa376932(v=VS.85).aspx">Error Handling</a>.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The <i>pszPrinterName</i> parameter must be the full name, not the truncated name as it may appear in a <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a>.

The first version of the Print Schema was released with Windows Vista and is version 1. If the print ticket provider does not support <i>prefVersion</i>, <b>PTOpenProviderEx</b> successfully opens a handle and returns an earlier version in <i>usedVersion</i>.

To avoid a resource leak, <i>phProvider</i> must be closed with <a href="https://msdn.microsoft.com/28e85b53-fd0c-4210-ae2b-794efaf65bd4">PTCloseProvider</a>.




## -see-also




<a href="https://msdn.microsoft.com/98d5f8ec-54bd-4e88-b632-ed427b599cb6">Print Schema</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/e5c115b0-9c1e-46e7-8fb5-eddbc2c75298">Printing</a>
 

 

