---
UID: NF:shlobj.IFileViewerA.PrintTo
title: IFileViewerA::PrintTo
description: Prints a file. (ANSI)
helpviewer_keywords: ["IFileViewerA::PrintTo"]
tech.root: shell
ms.assetid: 4a8fd0ed-4a9a-47c7-a0ab-87cf82f507cb
ms.date: 01/30/2019
ms.keywords: IFileViewerA::PrintTo
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: shlobj.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - IFileViewerA::PrintTo
 - shlobj/IFileViewerA::PrintTo
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - shlobj.h
api_name:
 - IFileViewerA::PrintTo
---

## -description

Prints a file. The Shell specifies the name of the file to print by calling the file viewer's [IPersistFile::Load](/windows/desktop/api/objidl/nf-objidl-ipersistfile-load) method.

## -parameters

### -param pszDriver

A pointer to a buffer that contains the name of the printer device driver that should print the file. If this parameter is **NULL**, the file viewer determines which device driver to use.

### -param fSuppressUI

A user interface suppression flag. If this parameter is **TRUE**, the file viewer should not display any user interface, including error messages, during the print operation. If this parameter is **FALSE**, the file viewer can show dialog boxes, as needed.

## -returns

## -remarks

## -see-also
