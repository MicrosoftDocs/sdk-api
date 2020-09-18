---
UID: NF:fdi.FDIDestroy
title: FDIDestroy function (fdi.h)
description: The FDIDestroy function deletes an open FDI context.
helpviewer_keywords: ["FDIDestroy","FDIDestroy function [Windows API]","fdi/FDIDestroy","winprog.fdidestroy"]
old-location: winprog\fdidestroy.htm
tech.root: winprog
ms.assetid: fe3b8045-a476-4a21-b732-0d4799798faf
ms.date: 12/05/2018
ms.keywords: FDIDestroy, FDIDestroy function [Windows API], fdi/FDIDestroy, winprog.fdidestroy
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
 - FDIDestroy
 - fdi/FDIDestroy
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
 - FDIDestroy
---

# FDIDestroy function


## -description

The <b>FDIDestroy</b> function deletes an open FDI context.

## -parameters

### -param hfdi [in]

 A valid FDI context handle returned by  the <a href="/windows/desktop/api/fdi/nf-fdi-fdicreate">FDICreate</a> function.

## -returns

If the function succeeds, it returns <b>TRUE</b>; otherwise, <b>FALSE</b>.

Extended error information is provided in the <a href="/windows/desktop/api/fdi_fci_types/ns-fdi_fci_types-erf">ERF</a> structure used to create the FDI context.

## -see-also

<a href="/windows/desktop/api/fdi/nf-fdi-fdicreate">FDICreate</a>