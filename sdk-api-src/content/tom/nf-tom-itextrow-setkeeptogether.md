---
UID: NF:tom.ITextRow.SetKeepTogether
title: ITextRow::SetKeepTogether (tom.h)
description: Sets whether this row is allowed to be broken across pages.
helpviewer_keywords: ["ITextRow interface [Windows Controls]","SetKeepTogether method","ITextRow.SetKeepTogether","ITextRow::SetKeepTogether","SetKeepTogether","SetKeepTogether method [Windows Controls]","SetKeepTogether method [Windows Controls]","ITextRow interface","controls.itextrow_setkeeptogether","tom/ITextRow::SetKeepTogether"]
old-location: controls\itextrow_setkeeptogether.htm
tech.root: Controls
ms.assetid: ca2130b4-3e29-43d7-b03d-a6c45897e447
ms.date: 12/05/2018
ms.keywords: ITextRow interface [Windows Controls],SetKeepTogether method, ITextRow.SetKeepTogether, ITextRow::SetKeepTogether, SetKeepTogether, SetKeepTogether method [Windows Controls], SetKeepTogether method [Windows Controls],ITextRow interface, controls.itextrow_setkeeptogether, tom/ITextRow::SetKeepTogether
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
 - ITextRow::SetKeepTogether
 - tom/ITextRow::SetKeepTogether
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
 - ITextRow.SetKeepTogether
---

# ITextRow::SetKeepTogether


## -description

Sets whether this row is allowed to be broken across pages.

## -parameters

### -param Value [in]

Type: <b>long</b>

A <a href="/windows/desktop/Controls/about-text-object-model">tomBool</a> value that indicates whether this row can be broken across pages.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-getkeeptogether">ITextRow::GetKeepTogether</a>