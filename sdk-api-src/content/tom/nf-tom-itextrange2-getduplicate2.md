---
UID: NF:tom.ITextRange2.GetDuplicate2
title: ITextRange2::GetDuplicate2 (tom.h)
description: Gets a duplicate of a range object.
helpviewer_keywords: ["GetDuplicate2","GetDuplicate2 method [Windows Controls]","GetDuplicate2 method [Windows Controls]","ITextRange2 interface","ITextRange2 interface [Windows Controls]","GetDuplicate2 method","ITextRange2.GetDuplicate2","ITextRange2::GetDuplicate2","controls.itextrange2_getduplicate2","tom/ITextRange2::GetDuplicate2"]
old-location: controls\itextrange2_getduplicate2.htm
tech.root: Controls
ms.assetid: 6dce56b6-463a-49d4-8e4b-397e2841544c
ms.date: 12/05/2018
ms.keywords: GetDuplicate2, GetDuplicate2 method [Windows Controls], GetDuplicate2 method [Windows Controls],ITextRange2 interface, ITextRange2 interface [Windows Controls],GetDuplicate2 method, ITextRange2.GetDuplicate2, ITextRange2::GetDuplicate2, controls.itextrange2_getduplicate2, tom/ITextRange2::GetDuplicate2
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
 - ITextRange2::GetDuplicate2
 - tom/ITextRange2::GetDuplicate2
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
 - ITextRange2.GetDuplicate2
---

# ITextRange2::GetDuplicate2


## -description

Gets a duplicate of a range object.

## -parameters

### -param ppRange [out, retval]

Type: <b>ITextRange2**</b>

The duplicate range.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If this range is an <a href="/windows/desktop/api/tom/nn-tom-itextselection2">ITextSelection2</a> object, the duplicate returned is an <a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a> object. See the <a href="/windows/desktop/api/tom/nf-tom-itextrange-findtext">ITextRange::FindText</a> method for more information.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>