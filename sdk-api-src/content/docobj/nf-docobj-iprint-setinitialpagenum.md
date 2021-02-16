---
UID: NF:docobj.IPrint.SetInitialPageNum
title: IPrint::SetInitialPageNum (docobj.h)
description: Sets the page number of the first page of a document.
helpviewer_keywords: ["IPrint interface [COM]","SetInitialPageNum method","IPrint.SetInitialPageNum","IPrint::SetInitialPageNum","SetInitialPageNum","SetInitialPageNum method [COM]","SetInitialPageNum method [COM]","IPrint interface","_ctrl_iprint_setinitialpagenum","com.iprint_setinitialpagenum","docobj/IPrint::SetInitialPageNum"]
old-location: com\iprint_setinitialpagenum.htm
tech.root: com
ms.assetid: 352a4dc0-c79e-46e3-8212-55fd7d2916bc
ms.date: 12/05/2018
ms.keywords: IPrint interface [COM],SetInitialPageNum method, IPrint.SetInitialPageNum, IPrint::SetInitialPageNum, SetInitialPageNum, SetInitialPageNum method [COM], SetInitialPageNum method [COM],IPrint interface, _ctrl_iprint_setinitialpagenum, com.iprint_setinitialpagenum, docobj/IPrint::SetInitialPageNum
req.header: docobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DocObj.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPrint::SetInitialPageNum
 - docobj/IPrint::SetInitialPageNum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DocObj.h
api_name:
 - IPrint.SetInitialPageNum
---

# IPrint::SetInitialPageNum


## -description

Sets the page number of the first page of a document.

## -parameters

### -param nFirstPage [in]

The page number of the first page.

## -returns

This method can return the standard return values E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

Setting the first page to a negative number is valid. This may be useful in printing a portion of the document with page numbers that specify an offset from the usual pagination.

Not all implementations permit the initial page number to be set, as some implementations simply lack the information as to how the page number should be presented in the final output.

## -see-also

<a href="/windows/desktop/api/docobj/nn-docobj-iprint">IPrint</a>