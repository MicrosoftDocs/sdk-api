---
UID: NF:fdi.FDICopy
title: FDICopy function (fdi.h)
description: The FDICopy function extracts files from cabinets.
helpviewer_keywords: ["FDICopy","FDICopy function [Windows API]","fdi/FDICopy","winprog.fdicopy"]
old-location: winprog\fdicopy.htm
tech.root: winprog
ms.assetid: 6ec2b10b-f70a-4a22-beff-df6b6a4c4cfd
ms.date: 12/05/2018
ms.keywords: FDICopy, FDICopy function [Windows API], fdi/FDICopy, winprog.fdicopy
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
 - FDICopy
 - fdi/FDICopy
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
 - FDICopy
---

# FDICopy function


## -description

The <b>FDICopy</b> function extracts files from cabinets.

## -parameters

### -param hfdi [in]

A valid FDI context handle returned by the <a href="/windows/desktop/api/fdi/nf-fdi-fdicreate">FDICreate</a> function.

### -param pszCabinet [in]

The name of the cabinet file, excluding any path information, from which to extract files. If a file is split over multiple cabinets, <b>FDICopy</b>  allows for subsequent cabinets to be opened.

### -param pszCabPath [in]

The pathname of the cabinet file, but not including the name of the file itself. For example, "C:\MyCabs\". 

The contents of <i>pszCabinet</i> are appended to <i>pszCabPath</i> to create the full pathname of the cabinet.

### -param flags [in]

No flags are currently defined and this parameter should be set to zero.

### -param pfnfdin [in]

Pointer to an application-defined callback notification function to update the application on the status of the decoder. The function should be declared using the <a href="/windows/desktop/api/fdi/nf-fdi-fnfdinotify">FNFDINOTIFY</a> macro.

### -param pfnfdid [in]

Not currently used by FDI. This parameter should be set to <b>NULL</b>.

### -param pvUser [in, optional]

Pointer to an application-specified value to pass to the notification function.

## -returns

If the function succeeds, it returns <b>TRUE</b>; otherwise, <b>FALSE</b>.

Extended error information is provided in the <a href="/windows/desktop/api/fdi_fci_types/ns-fdi_fci_types-erf">ERF</a> structure used to create the FDI context.

## -see-also

<a href="/windows/desktop/api/fdi/nf-fdi-fdicreate">FDICreate</a>