---
UID: NF:prntvpt.PTOpenProvider
title: PTOpenProvider function (prntvpt.h)
description: Opens an instance of a print ticket provider. (PTOpenProvider)
helpviewer_keywords: ["PTOpenProvider","PTOpenProvider function [Windows GDI]","_win32_PTOpenProvider","gdi.ptopenprovider","prntvpt/PTOpenProvider"]
old-location: gdi\ptopenprovider.htm
tech.root: xps
ms.assetid: 6821b1b0-74b0-4caf-b8e6-a9df4d7693d7
ms.date: 12/05/2018
ms.keywords: PTOpenProvider, PTOpenProvider function [Windows GDI], _win32_PTOpenProvider, gdi.ptopenprovider, prntvpt/PTOpenProvider
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
 - PTOpenProvider
 - prntvpt/PTOpenProvider
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
 - PTOpenProvider
---

# PTOpenProvider function


## -description

Opens an instance of a print ticket provider.

## -parameters

### -param pszPrinterName [in]

A pointer to the full name of a print queue.

### -param dwVersion

The version of the <a href="/windows/desktop/printdocs/printschema">Print Schema</a> requested by the caller.

### -param phProvider [out]

A pointer to a handle for the provider.

## -returns

If the operation succeeds, the return value is S_OK, otherwise the <b>HRESULT</b> contains an error code.

For more information about COM error codes, see <a href="/windows/desktop/SetupApi/error-handling">Error Handling</a>.

## -remarks

<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
<i>pszPrinterName</i> must be the full name, not the truncated name as it may appear in a <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a>.

The first version of the Print Schema was released with Windows Vista and is version 1. This operation fails if <i>version</i> is not supported. Contrast this with <a href="/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex">PTOpenProviderEx</a> which opens a provider even if it supports only versions that are earlier than requested.

To avoid a resource leak, <i>phProvider</i> must be closed with <a href="/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider">PTCloseProvider</a>.

## -see-also

<a href="/windows/desktop/printdocs/printschema">Print Schema</a>



<a href="/windows/desktop/printdocs/printing-and-print-spooler-functions">Print Spooler API Functions</a>



<a href="/windows/desktop/printdocs/printdocs-printing">Printing</a>
