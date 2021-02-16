---
UID: NF:tom.ITextRow.GetKeepWithNext
title: ITextRow::GetKeepWithNext (tom.h)
description: Gets whether this row should appear on the same page as the row that follows it.
helpviewer_keywords: ["GetKeepWithNext","GetKeepWithNext method [Windows Controls]","GetKeepWithNext method [Windows Controls]","ITextRow interface","ITextRow interface [Windows Controls]","GetKeepWithNext method","ITextRow.GetKeepWithNext","ITextRow::GetKeepWithNext","controls.itextrow_getkeepwithnext","tom/ITextRow::GetKeepWithNext"]
old-location: controls\itextrow_getkeepwithnext.htm
tech.root: Controls
ms.assetid: 67c5f06c-9f45-430b-ae9f-0ca1931df411
ms.date: 12/05/2018
ms.keywords: GetKeepWithNext, GetKeepWithNext method [Windows Controls], GetKeepWithNext method [Windows Controls],ITextRow interface, ITextRow interface [Windows Controls],GetKeepWithNext method, ITextRow.GetKeepWithNext, ITextRow::GetKeepWithNext, controls.itextrow_getkeepwithnext, tom/ITextRow::GetKeepWithNext
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
 - ITextRow::GetKeepWithNext
 - tom/ITextRow::GetKeepWithNext
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
 - ITextRow.GetKeepWithNext
---

# ITextRow::GetKeepWithNext


## -description

Gets  whether this row should appear on the same page as the row that follows it.

## -parameters

### -param pValue [out, retval]

Type: <b>long*</b>

A <a href="/windows/desktop/Controls/about-text-object-model">tomBool</a> value that indicates whether this row should be kept on the same page as the following row.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-setkeepwithnext">ITextRow::SetKeepWithNext</a>