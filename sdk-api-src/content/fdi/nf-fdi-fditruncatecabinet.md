---
UID: NF:fdi.FDITruncateCabinet
title: FDITruncateCabinet function (fdi.h)
description: The FDITruncateCabinet function truncates a cabinet file starting at the specified folder number.
helpviewer_keywords: ["FDITruncateCabinet","FDITruncateCabinet function [Windows API]","fdi/FDITruncateCabinet","winprog.fditruncatecabinet"]
old-location: winprog\fditruncatecabinet.htm
tech.root: winprog
ms.assetid: c923b0a5-1a8d-42aa-bd05-0d318199756d
ms.date: 12/05/2018
ms.keywords: FDITruncateCabinet, FDITruncateCabinet function [Windows API], fdi/FDITruncateCabinet, winprog.fditruncatecabinet
req.header: fdi.h
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
 - FDITruncateCabinet
 - fdi/FDITruncateCabinet
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
 - FDITruncateCabinet
---

# FDITruncateCabinet function


## -description

The <b>FDITruncateCabinet</b> function truncates a cabinet file starting at the specified folder number.

## -parameters

### -param hfdi [in]

A valid FDI context handle returned by the <a href="/windows/desktop/api/fdi/nf-fdi-fdicreate">FDICreate</a> function.

### -param pszCabinetName [in]

The full cabinet filename.

### -param iFolderToDelete [in]

The index of the first folder to delete.

## -returns

If the function succeeds, it returns <b>TRUE</b>; otherwise, <b>FALSE</b>.

Extended error information is provided in the <a href="/windows/desktop/api/fdi_fci_types/ns-fdi_fci_types-erf">ERF</a> structure used to create the FDI context.

## -see-also

<a href="/windows/desktop/api/fdi/nf-fdi-fdiiscabinet">FDIIsCabinet</a>