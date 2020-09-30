---
UID: NF:tom.ITextRow.GetKeepTogether
title: ITextRow::GetKeepTogether (tom.h)
description: Gets whether this row is allowed to be broken across pages.
helpviewer_keywords: ["GetKeepTogether","GetKeepTogether method [Windows Controls]","GetKeepTogether method [Windows Controls]","ITextRow interface","ITextRow interface [Windows Controls]","GetKeepTogether method","ITextRow.GetKeepTogether","ITextRow::GetKeepTogether","controls.itextrow_getkeeptogether","tom/ITextRow::GetKeepTogether"]
old-location: controls\itextrow_getkeeptogether.htm
tech.root: Controls
ms.assetid: 3f40c910-2636-4412-ae05-7a630c1f4806
ms.date: 12/05/2018
ms.keywords: GetKeepTogether, GetKeepTogether method [Windows Controls], GetKeepTogether method [Windows Controls],ITextRow interface, ITextRow interface [Windows Controls],GetKeepTogether method, ITextRow.GetKeepTogether, ITextRow::GetKeepTogether, controls.itextrow_getkeeptogether, tom/ITextRow::GetKeepTogether
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
 - ITextRow::GetKeepTogether
 - tom/ITextRow::GetKeepTogether
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
 - ITextRow.GetKeepTogether
---

# ITextRow::GetKeepTogether


## -description

Gets whether this row is allowed to be broken across pages.

## -parameters

### -param pValue [out, retval]

Type: <b>long*</b>

A <a href="/windows/desktop/Controls/about-text-object-model">tomBool</a> value that indicates whether this row can be broken across pages.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-setkeeptogether">ITextRow::SetKeepTogether</a>