---
UID: NF:fdi.FDIIsCabinet
title: FDIIsCabinet function (fdi.h)
description: The FDIIsCabinet function determines whether a file is a cabinet and, if it is, returns information about it.
helpviewer_keywords: ["FDIIsCabinet","FDIIsCabinet function [Windows API]","fdi/FDIIsCabinet","winprog.fdiiscabinet"]
old-location: winprog\fdiiscabinet.htm
tech.root: winprog
ms.assetid: 01d223ca-56c6-49fa-b9e6-e5eeda88936a
ms.date: 12/05/2018
ms.keywords: FDIIsCabinet, FDIIsCabinet function [Windows API], fdi/FDIIsCabinet, winprog.fdiiscabinet
req.header: fdi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - FDIIsCabinet
 - fdi/FDIIsCabinet
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
 - FDIIsCabinet
---

# FDIIsCabinet function


## -description

The <b>FDIIsCabinet</b> function determines whether a file is a cabinet and, if it is, returns information about it.

## -parameters

### -param hfdi [in]

A valid FDI context handle returned  by <a href="/windows/desktop/api/fdi/nf-fdi-fdicreate">FDICreate</a>.

### -param hf [in]

An application-defined value to keep track of the opened file. This value must be of the same type as values used by the File I/O functions passed to <a href="/windows/desktop/api/fdi/nf-fdi-fdicreate">FDICreate</a>.

### -param pfdici [in, out]

Pointer to an <a href="/windows/desktop/api/fdi/ns-fdi-fdicabinetinfo">FDICABINETINFO</a> structure that receives the cabinet details, in the event the file is actually a cabinet.

## -returns

If the file is a cabinet, the function returns <b>TRUE</b> ; otherwise, <b>FALSE</b>.

Extended error information is provided in the <a href="/windows/desktop/api/fdi_fci_types/ns-fdi_fci_types-erf">ERF</a> structure used to create the FDI context.

## -see-also

<a href="/windows/desktop/api/fdi/ns-fdi-fdicabinetinfo">FDICABINETINFO</a>



<a href="/windows/desktop/api/fdi/nf-fdi-fdicreate">FDICreate</a>



<a href="/windows/desktop/api/fdi/nf-fdi-fditruncatecabinet">FDITruncateCabinet</a>