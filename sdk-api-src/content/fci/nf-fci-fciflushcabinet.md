---
UID: NF:fci.FCIFlushCabinet
title: FCIFlushCabinet function (fci.h)
description: The FCIFlushCabinet function completes the current cabinet.
helpviewer_keywords: ["FCIFlushCabinet","FCIFlushCabinet function [Windows API]","fci/FCIFlushCabinet","winprog.fciflushcabinet"]
old-location: winprog\fciflushcabinet.htm
tech.root: winprog
ms.assetid: dc586260-180e-4a6b-accf-2ddd62ac1335
ms.date: 12/05/2018
ms.keywords: FCIFlushCabinet, FCIFlushCabinet function [Windows API], fci/FCIFlushCabinet, winprog.fciflushcabinet
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
 - FCIFlushCabinet
 - fci/FCIFlushCabinet
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
 - FCIFlushCabinet
---

# FCIFlushCabinet function


## -description

The <b>FCIFlushCabinet</b> function completes the current cabinet.

## -parameters

### -param hfci [in]

A valid FCI context handle returned by the<a href="/windows/desktop/api/fci/nf-fci-fcicreate">FCICreate</a> function.

### -param fGetNextCab [in]

Specifies whether the function pointed to by the supplied <i>GetNextCab</i> parameter will be called.

### -param pfnfcignc [in]

Pointer to an application-defined callback function to obtain specifications on the next cabinet to create. The function should be declared using the <a href="/windows/desktop/api/fci/nf-fci-fnfcigetnextcabinet">FNFCIGETNEXTCABINET</a> macro.

### -param pfnfcis [in]

Pointer to an application-defined callback function to update the user. The function should be declared using the <a href="/windows/desktop/api/fci/nf-fci-fnfcistatus">FNFCISTATUS</a> macro.

## -returns

If the function succeeds, it returns <b>TRUE</b>; otherwise, <b>FALSE</b>.

Extended error information is provided in the <a href="/windows/desktop/api/fdi_fci_types/ns-fdi_fci_types-erf">ERF</a> structure used to create the FCI context.

## -remarks

The <b>FCIFlushCabinet</b> API forces the current cabinet under construction to be completed immediately and then written to disk. Further calls to <a href="/windows/desktop/api/fci/nf-fci-fciaddfile">FCIAddFile</a> will result in files being added to another cabinet.

 In the event the current cabinet has reached the application-specified media size limit, the pending data within an FCI's internal buffers will be placed into another cabinet.

The <i>fGetNextCab</i> flag determines whether the function pointed to by the <i>GetNextCab</i> parameter will be called. If <i>fGetNextCab</i> is set <b>TRUE</b>, <i>GetNextCab</i> is called to obtain continuation information. If <b>FALSE</b>, then <i>GetNextCab</i> is called only in the event the cabinet overflows.

## -see-also

<a href="/windows/desktop/api/fci/nf-fci-fciflushfolder">FCIFlushFolder</a>