---
UID: NF:fci.FCIDestroy
title: FCIDestroy function (fci.h)
description: The FCIDestroy function deletes an open FCI context, freeing any memory and temporary files associated with the context.
helpviewer_keywords: ["FCIDestroy","FCIDestroy function [Windows API]","fci/FCIDestroy","winprog.fcidestroy"]
old-location: winprog\fcidestroy.htm
tech.root: DevNotes
ms.assetid: bb1a6294-664f-450f-b8ec-d6f8957d920e
ms.date: 12/05/2018
ms.keywords: FCIDestroy, FCIDestroy function [Windows API], fci/FCIDestroy, winprog.fcidestroy
f1_keywords:
- fci/FCIDestroy
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Cabinet.dll
api_name:
- FCIDestroy
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FCIDestroy function


## -description


The <b>FCIDestroy</b> function deletes an open  FCI context, freeing any memory and temporary files associated with the context.


## -parameters




### -param hfci [in]

A valid FCI context handle returned by the <a href="https://docs.microsoft.com/windows/desktop/api/fci/nf-fci-fcicreate">FCICreate</a> function.


## -returns



If the function succeeds, it returns <b>TRUE</b>; otherwise, <b>FALSE</b>.

Extended error information is provided in the <a href="https://docs.microsoft.com/windows/desktop/api/fdi_fci_types/ns-fdi_fci_types-erf">ERF</a> structure used to create the FCI context.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fci/nf-fci-fcicreate">FCICreate</a>
 

 

