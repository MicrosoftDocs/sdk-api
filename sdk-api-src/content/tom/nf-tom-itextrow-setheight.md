---
UID: NF:tom.ITextRow.SetHeight
title: ITextRow::SetHeight (tom.h)
description: Sets the height of a row.
helpviewer_keywords: ["ITextRow interface [Windows Controls]","SetHeight method","ITextRow.SetHeight","ITextRow::SetHeight","SetHeight","SetHeight method [Windows Controls]","SetHeight method [Windows Controls]","ITextRow interface","controls.itextrow_setheight","tom/ITextRow::SetHeight"]
old-location: controls\itextrow_setheight.htm
tech.root: Controls
ms.assetid: c377bdef-d906-4f7b-98f0-13633906ced9
ms.date: 12/05/2018
ms.keywords: ITextRow interface [Windows Controls],SetHeight method, ITextRow.SetHeight, ITextRow::SetHeight, SetHeight, SetHeight method [Windows Controls], SetHeight method [Windows Controls],ITextRow interface, controls.itextrow_setheight, tom/ITextRow::SetHeight
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
 - ITextRow::SetHeight
 - tom/ITextRow::SetHeight
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
 - ITextRow.SetHeight
---

# ITextRow::SetHeight


## -description

Sets the height of a row.

## -parameters

### -param Value [in]

Type: <b>long</b>

The row height. A value of 0 indicates autoheight.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-getheight">ITextRow::GetHeight</a>