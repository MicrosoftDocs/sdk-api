---
UID: NF:prntvpt.PTQuerySchemaVersionSupport
title: PTQuerySchemaVersionSupport function
author: windows-sdk-content
description: Retrieves the highest (latest) version of the Print Schema that the specified printer supports.
old-location: gdi\ptqueryschemaversionsupport.htm
old-project: printdocs
ms.assetid: a3b5a92f-3a5b-4438-b788-91c9ac5a191f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PTQuerySchemaVersionSupport, PTQuerySchemaVersionSupport function [Windows GDI], _win32_PTQuerySchemaVersionSupport, gdi.ptqueryschemaversionsupport, prntvpt/PTQuerySchemaVersionSupport
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: prntvpt.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: EDefaultDevmodeType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - prntvpt.dll
 - Ext-MS-Win-printer-prntvpt-l1-1-0.dll
api_name:
 - PTQuerySchemaVersionSupport
product: Windows
targetos: Windows
req.lib: Prntvpt.lib
req.dll: Prntvpt.dll
req.irql: 
req.product: ADAM
---

# PTQuerySchemaVersionSupport function


## -description


Retrieves the highest (latest) version of the <a href="https://msdn.microsoft.com/98d5f8ec-54bd-4e88-b632-ed427b599cb6">Print Schema</a> that the specified printer supports.


## -parameters




### -param pszPrinterName [in]

A pointer to the full name of a print queue.


### -param pMaxVersion [out]

A pointer to the highest version.


## -returns



If the operation succeeds, the return value is S_OK, otherwise the <b>HRESULT</b> contains an error code.

For more information about COM error codes, see <a href="_com_error_handling">Error Handling</a>.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The <i>pszPrinterName</i> parameter must be the full name, not the truncated name as it may appear in a <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a>.

The first version of the Print Schema was released with Windows Vista and is version 1.




## -see-also




<a href="https://msdn.microsoft.com/98d5f8ec-54bd-4e88-b632-ed427b599cb6">Print Schema</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/e5c115b0-9c1e-46e7-8fb5-eddbc2c75298">Printing</a>
 

 

