---
UID: NF:fci.FCIFlushFolder
title: FCIFlushFolder function (fci.h)
description: The FCIFlushFolder function forces the current folder under construction to be completed immediately.
helpviewer_keywords: ["FCIFlushFolder","FCIFlushFolder function [Windows API]","fci/FCIFlushFolder","winprog.fciflushfolder"]
old-location: winprog\fciflushfolder.htm
tech.root: winprog
ms.assetid: dc9c226e-e309-48c3-9edb-3f0a040c0c18
ms.date: 12/05/2018
ms.keywords: FCIFlushFolder, FCIFlushFolder function [Windows API], fci/FCIFlushFolder, winprog.fciflushfolder
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
 - FCIFlushFolder
 - fci/FCIFlushFolder
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
 - FCIFlushFolder
---

# FCIFlushFolder function


## -description

The <b>FCIFlushFolder</b> function forces the current folder under construction to be completed immediately.

## -parameters

### -param hfci [in]

A valid FCI context handle returned by the <a href="/windows/desktop/api/fci/nf-fci-fcicreate">FCICreate</a> function.

### -param pfnfcignc [in]

Pointer to an application-defined callback function to obtain specifications on the next cabinet to create. The function should be declared using the <a href="/windows/desktop/api/fci/nf-fci-fnfcigetnextcabinet">FNFCIGETNEXTCABINET</a> macro.

### -param pfnfcis [in]

Pointer to an application-defined callback function to update the user. The function should be declared using the <a href="/windows/desktop/api/fci/nf-fci-fnfcistatus">FNFCISTATUS</a> macro.

## -returns

If the function succeeds, it returns <b>TRUE</b>; otherwise, <b>FALSE</b>.

Extended error information is provided in the <a href="/windows/desktop/api/fdi_fci_types/ns-fdi_fci_types-erf">ERF</a> structure used to create the FCI context.

## -remarks

The <b>FCIFlushFolder</b> API forces the folder currently under construction to be completed immediately; effectively resetting the compression history if a compression method is in use.

The callback function indicated by <i>GetNextCab</i> will be called if the cabinet overflows, which occurs if the pending data buffered inside an FCI causes the application-specified cabinet media size to be exceeded.

## -see-also

<a href="/windows/desktop/api/fci/nf-fci-fciflushcabinet">FCIFlushCabinet</a>