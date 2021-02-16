---
UID: NF:docobj.IPrint.GetPageInfo
title: IPrint::GetPageInfo (docobj.h)
description: Retrieves the number of a document's first page and the total number of pages.
helpviewer_keywords: ["GetPageInfo","GetPageInfo method [COM]","GetPageInfo method [COM]","IPrint interface","IPrint interface [COM]","GetPageInfo method","IPrint.GetPageInfo","IPrint::GetPageInfo","_ctrl_iprint_getpageinfo","com.iprint_getpageinfo","docobj/IPrint::GetPageInfo"]
old-location: com\iprint_getpageinfo.htm
tech.root: com
ms.assetid: 8f3a2d21-5345-4c4e-9928-37dcd6ec5fcc
ms.date: 12/05/2018
ms.keywords: GetPageInfo, GetPageInfo method [COM], GetPageInfo method [COM],IPrint interface, IPrint interface [COM],GetPageInfo method, IPrint.GetPageInfo, IPrint::GetPageInfo, _ctrl_iprint_getpageinfo, com.iprint_getpageinfo, docobj/IPrint::GetPageInfo
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
 - IPrint::GetPageInfo
 - docobj/IPrint::GetPageInfo
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
 - IPrint.GetPageInfo
---

# IPrint::GetPageInfo


## -description

Retrieves the number of a document's first page and the total number of pages.

## -parameters

### -param pnFirstPage [out]

A pointer to a variable that receives the page number of the first page. This parameter can be <b>NULL</b>, indicating that the caller is not interested in this number. If <a href="/windows/desktop/api/docobj/nf-docobj-iprint-setinitialpagenum">IPrint::SetInitialPageNum</a> has been called, this parameter should contain the same value passed to that method. Otherwise, the value is the document's internal first page number.

### -param pcPages [out]

A pointer to a variable that receives the total number of pages in this document. This parameter can be <b>NULL</b>, indicating that the caller is not interested in this number.

## -returns

This method can return the standard return values E_UNEXPECTED and S_OK.

## -see-also

<a href="/windows/desktop/api/docobj/nn-docobj-iprint">IPrint</a>