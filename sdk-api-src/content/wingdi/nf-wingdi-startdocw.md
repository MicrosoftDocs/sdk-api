---
UID: NF:wingdi.StartDocW
title: StartDocW function (wingdi.h)
description: The StartDoc function starts a print job. (Unicode)
helpviewer_keywords: ["StartDoc", "StartDoc function [Windows GDI]", "StartDocW", "_win32_StartDoc", "gdi.startdoc", "wingdi/StartDoc", "wingdi/StartDocW"]
old-location: gdi\startdoc.htm
tech.root: xps
ms.assetid: 53143463-b9fc-4378-aea9-da6c73a7cd03
ms.date: 12/05/2018
ms.keywords: StartDoc, StartDoc function [Windows GDI], StartDocA, StartDocW, _win32_StartDoc, gdi.startdoc, wingdi/StartDoc, wingdi/StartDocA, wingdi/StartDocW
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StartDocW (Unicode) and StartDocA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - StartDocW
 - wingdi/StartDocW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-print-l1-1-0.dll
 - GDI32Full.dll
api_name:
 - StartDoc
 - StartDocA
 - StartDocW
---

# StartDocW function


## -description

The <b>StartDoc</b> function starts a print job.

## -parameters

### -param hdc [in]

A handle to the device context for the print job.

### -param lpdi [in]

A pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-docinfow">DOCINFO</a> structure containing the name of the document file and the name of the output file.

## -returns

If the function succeeds, the return value is greater than zero. This value is the print job identifier for the document.

If the function fails, the return value is less than or equal to zero.

## -remarks

<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
Applications should call the <b>StartDoc</b> function immediately before beginning a print job. Using this function ensures that multipage documents are not interspersed with other print jobs.

Applications can use the value returned by <b>StartDoc</b> to retrieve or set the priority of a print job. Call the <a href="/windows/desktop/printdocs/getjob">GetJob</a> or <a href="/windows/desktop/printdocs/setjob">SetJob</a> function and supply this value as one of the required arguments.


#### Examples

For a sample program that uses this function, see <a href="/windows/desktop/printdocs/how-to--print-using-the-gdi-print-api">How To: Print Using the GDI Print API</a>.

<div class="code"></div>




> [!NOTE]
> The wingdi.h header defines StartDoc as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-docinfoa">DOCINFO</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-enddoc">EndDoc</a>



<a href="/windows/desktop/printdocs/getjob">GetJob</a>



<a href="/windows/desktop/printdocs/printing-and-print-spooler-functions">Print Spooler API Functions</a>



<a href="/windows/desktop/printdocs/printdocs-printing">Printing</a>



<a href="/windows/desktop/printdocs/setjob">SetJob</a>
