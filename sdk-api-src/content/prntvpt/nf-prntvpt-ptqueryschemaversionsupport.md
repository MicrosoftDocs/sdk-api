---
UID: NF:prntvpt.PTQuerySchemaVersionSupport
title: PTQuerySchemaVersionSupport function (prntvpt.h)
description: Retrieves the highest (latest) version of the Print Schema that the specified printer supports.
helpviewer_keywords: ["PTQuerySchemaVersionSupport","PTQuerySchemaVersionSupport function [Windows GDI]","_win32_PTQuerySchemaVersionSupport","gdi.ptqueryschemaversionsupport","prntvpt/PTQuerySchemaVersionSupport"]
old-location: gdi\ptqueryschemaversionsupport.htm
tech.root: xps
ms.assetid: a3b5a92f-3a5b-4438-b788-91c9ac5a191f
ms.date: 12/05/2018
ms.keywords: PTQuerySchemaVersionSupport, PTQuerySchemaVersionSupport function [Windows GDI], _win32_PTQuerySchemaVersionSupport, gdi.ptqueryschemaversionsupport, prntvpt/PTQuerySchemaVersionSupport
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PTQuerySchemaVersionSupport
 - prntvpt/PTQuerySchemaVersionSupport
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-printer-prntvpt-l1-1-2.dll
 - ext-ms-win-printer-prntvpt-l1-1-1.dll
 - prntvpt.dll
 - Ext-MS-Win-printer-prntvpt-l1-1-0.dll
api_name:
 - PTQuerySchemaVersionSupport
---

# PTQuerySchemaVersionSupport function


## -description

Retrieves the highest (latest) version of the <a href="/windows/desktop/printdocs/printschema">Print Schema</a> that the specified printer supports.

## -parameters

### -param pszPrinterName [in]

A pointer to the full name of a print queue.

### -param pMaxVersion [out]

A pointer to the highest version.

## -returns

If the operation succeeds, the return value is S_OK, otherwise the <b>HRESULT</b> contains an error code.

For more information about COM error codes, see <a href="/windows/desktop/SetupApi/error-handling">Error Handling</a>.

## -remarks

<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The <i>pszPrinterName</i> parameter must be the full name, not the truncated name as it may appear in a <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a>.

The first version of the Print Schema was released with Windows Vista and is version 1.

## -see-also

<a href="/windows/desktop/printdocs/printschema">Print Schema</a>



<a href="/windows/desktop/printdocs/printing-and-print-spooler-functions">Print Spooler API Functions</a>



<a href="/windows/desktop/printdocs/printdocs-printing">Printing</a>