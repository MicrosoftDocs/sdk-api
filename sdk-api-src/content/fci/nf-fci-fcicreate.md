---
UID: NF:fci.FCICreate
title: FCICreate function (fci.h)
description: The FCICreate function creates an FCI context.
helpviewer_keywords: ["FCICreate","FCICreate function [Windows API]","fci/FCICreate","winprog.fcicreate"]
old-location: winprog\fcicreate.htm
tech.root: winprog
ms.assetid: bfcea06d-2f09-405c-955c-0f56149148f2
ms.date: 12/05/2018
ms.keywords: FCICreate, FCICreate function [Windows API], fci/FCICreate, winprog.fcicreate
req.header: fci.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Cabinet.lib
req.dll: Cabinet.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FCICreate
 - fci/FCICreate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cabinet.dll
api_name:
 - FCICreate
---

# FCICreate function


## -description

The <b>FCICreate</b> function creates an FCI context.

## -parameters

### -param perf [in, out]

Pointer to an <a href="/windows/desktop/api/fdi_fci_types/ns-fdi_fci_types-erf">ERF</a> structure that receives the error information.

### -param pfnfcifp [in]

Pointer to an application-defined callback function to notify when a file is placed in the cabinet. The function should be declared using the <a href="/windows/desktop/api/fci/nf-fci-fnfcifileplaced">FNFCIFILEPLACED</a> macro.

### -param pfna [in]

Pointer to an application-defined callback function to allocate memory. The function should be declared using the <a href="/windows/desktop/api/fci/nf-fci-fnfcialloc">FNFCIALLOC</a> macro.

### -param pfnf [in]

Pointer to an application-defined callback function to free previously allocated memory. The function should be declared using the <a href="/windows/desktop/api/fci/nf-fci-fnfcifree">FNFCIFREE</a> macro.

### -param pfnopen [in]

Pointer to an application-defined callback function to open a file. The function should be declared using the <a href="/windows/desktop/api/fci/nf-fci-fnfciopen">FNFCIOPEN</a> macro.

### -param pfnread [in]

Pointer to an application-defined callback function to read data from a file. The function should be declared using the <a href="/windows/desktop/api/fci/nf-fci-fnfciread">FNFCIREAD</a> macro.

### -param pfnwrite [in]

Pointer to an application-defined callback function to write data to a file. The function should be declared using the <a href="/windows/desktop/api/fci/nf-fci-fnfciwrite">FNFCIWRITE</a> macro.

### -param pfnclose [in]

Pointer to an application-defined callback function to close a file. The function should be declared using the <a href="/windows/desktop/api/fci/nf-fci-fnfciclose">FNFCICLOSE</a> macro.

### -param pfnseek [in]

Pointer to an application-defined callback function to move a file pointer to the specific location. The function should be declared using the <a href="/windows/desktop/api/fci/nf-fci-fnfciseek">FNFCISEEK</a> macro.

### -param pfndelete [in]

Pointer to an application-defined callback function to delete a file. The function should be declared using the <a href="/windows/desktop/api/fci/nf-fci-fnfcidelete">FNFCIDELETE</a> macro.

### -param pfnfcigtf [in]

Pointer to an application-defined callback function to retrieve a temporary file name. The function should be declared using the <a href="/windows/desktop/api/fci/nf-fci-fnfcigettempfile">FNFCIGETTEMPFILE</a> macro.

### -param pccab [in]

Pointer to a <a href="/windows/desktop/api/fci/ns-fci-ccab">CCAB</a> structure that contains the parameters for creating a cabinet.

### -param pv [in, optional]

Pointer to an application-defined value that is passed to callback functions.

## -returns

If the function succeeds, it returns a non-<b>NULL</b> HFCI context pointer; otherwise, <b>NULL</b>.

Extended error information is provided in the <a href="/windows/desktop/api/fdi_fci_types/ns-fdi_fci_types-erf">ERF</a> structure.

## -remarks

FCI supports multiple simultaneous contexts. As a result it is possible to create or extract multiple cabinets at the same time within the same application. If the application is multithreaded, it is also possible to run a different context in each thread; however, an application cannot use the same context simultaneously in multiple threads. For example, <a href="/windows/desktop/api/fci/nf-fci-fciaddfile">FCIAddFile</a> cannot be called from two different threads, using the same FCI context.

## -see-also

<a href="/windows/desktop/api/fci/nf-fci-fciaddfile">FCIAddFile</a>



<a href="/windows/desktop/api/fci/nf-fci-fcidestroy">FCIDestroy</a>



<a href="/windows/desktop/api/fci/nf-fci-fciflushfolder">FCIFlushFolder</a>