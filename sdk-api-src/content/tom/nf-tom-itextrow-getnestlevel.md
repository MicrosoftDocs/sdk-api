---
UID: NF:tom.ITextRow.GetNestLevel
title: ITextRow::GetNestLevel (tom.h)
description: Gets the nest level of a table.
helpviewer_keywords: ["GetNestLevel","GetNestLevel method [Windows Controls]","GetNestLevel method [Windows Controls]","ITextRow interface","ITextRow interface [Windows Controls]","GetNestLevel method","ITextRow.GetNestLevel","ITextRow::GetNestLevel","controls.itextrow_getnestlevel","tom/ITextRow::GetNestLevel"]
old-location: controls\itextrow_getnestlevel.htm
tech.root: Controls
ms.assetid: 6b689344-6748-49d7-aa98-a87435b7cb0b
ms.date: 12/05/2018
ms.keywords: GetNestLevel, GetNestLevel method [Windows Controls], GetNestLevel method [Windows Controls],ITextRow interface, ITextRow interface [Windows Controls],GetNestLevel method, ITextRow.GetNestLevel, ITextRow::GetNestLevel, controls.itextrow_getnestlevel, tom/ITextRow::GetNestLevel
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextRow::GetNestLevel
 - tom/ITextRow::GetNestLevel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextRow.GetNestLevel
---

# ITextRow::GetNestLevel


## -description

Gets the nest level of a table.

## -parameters

### -param pValue [out, retval]

Type: <b>long*</b>

The nest level.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The nest level of the table is identified by the associated <a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a> object. If there is only a single table, the nest level is 1. If there is no table, the nest level is 0.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>