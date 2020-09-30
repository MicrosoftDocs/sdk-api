---
UID: NF:tom.ITextRow.SetKeepWithNext
title: ITextRow::SetKeepWithNext (tom.h)
description: Sets whether a row should appear on the same page as the row that follows it.
helpviewer_keywords: ["ITextRow interface [Windows Controls]","SetKeepWithNext method","ITextRow.SetKeepWithNext","ITextRow::SetKeepWithNext","SetKeepWithNext","SetKeepWithNext method [Windows Controls]","SetKeepWithNext method [Windows Controls]","ITextRow interface","controls.itextrow_setkeepwithnext","tom/ITextRow::SetKeepWithNext"]
old-location: controls\itextrow_setkeepwithnext.htm
tech.root: Controls
ms.assetid: 9b73ca91-39a1-4dee-8414-57ee45653c07
ms.date: 12/05/2018
ms.keywords: ITextRow interface [Windows Controls],SetKeepWithNext method, ITextRow.SetKeepWithNext, ITextRow::SetKeepWithNext, SetKeepWithNext, SetKeepWithNext method [Windows Controls], SetKeepWithNext method [Windows Controls],ITextRow interface, controls.itextrow_setkeepwithnext, tom/ITextRow::SetKeepWithNext
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
 - ITextRow::SetKeepWithNext
 - tom/ITextRow::SetKeepWithNext
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
 - ITextRow.SetKeepWithNext
---

# ITextRow::SetKeepWithNext


## -description

Sets whether a row should appear on the same page as the row that follows it.

## -parameters

### -param Value [in]

Type: <b>long</b>

A <a href="/windows/desktop/Controls/about-text-object-model">tomBool</a> value that indicates whether a row should appear on the same page as the row that follows it.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-getkeepwithnext">ITextRow::GetKeepWithNext</a>