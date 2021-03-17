---
UID: NF:tom.ITextRow.GetRTL
title: ITextRow::GetRTL (tom.h)
description: Gets whether this row has right-to-left orientation.
helpviewer_keywords: ["GetRTL","GetRTL method [Windows Controls]","GetRTL method [Windows Controls]","ITextRow interface","ITextRow interface [Windows Controls]","GetRTL method","ITextRow.GetRTL","ITextRow::GetRTL","controls.itextrow_getrtl","tom/ITextRow::GetRTL"]
old-location: controls\itextrow_getrtl.htm
tech.root: Controls
ms.assetid: 60261327-71f1-4bc3-97ac-b9c5ee3d44c0
ms.date: 12/05/2018
ms.keywords: GetRTL, GetRTL method [Windows Controls], GetRTL method [Windows Controls],ITextRow interface, ITextRow interface [Windows Controls],GetRTL method, ITextRow.GetRTL, ITextRow::GetRTL, controls.itextrow_getrtl, tom/ITextRow::GetRTL
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
 - ITextRow::GetRTL
 - tom/ITextRow::GetRTL
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
 - ITextRow.GetRTL
---

# ITextRow::GetRTL


## -description

Gets whether this row has right-to-left orientation.

## -parameters

### -param pValue [out, retval]

Type: <b>long*</b>

 A <a href="/windows/desktop/Controls/about-text-object-model">tomBool</a> value that indicates whether this row has right-to-left orientation.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-setrtl">ITextRow::SetRTL</a>