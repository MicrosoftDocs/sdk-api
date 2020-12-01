---
UID: NF:tom.ITextRange2.DeleteSubrange
title: ITextRange2::DeleteSubrange (tom.h)
description: Deletes a subrange from a range.
helpviewer_keywords: ["DeleteSubrange","DeleteSubrange method [Windows Controls]","DeleteSubrange method [Windows Controls]","ITextRange2 interface","ITextRange2 interface [Windows Controls]","DeleteSubrange method","ITextRange2.DeleteSubrange","ITextRange2::DeleteSubrange","controls.itextrange2_deletesubrange","tom/ITextRange2::DeleteSubrange"]
old-location: controls\itextrange2_deletesubrange.htm
tech.root: Controls
ms.assetid: ad75725d-ad92-45fc-a0a9-3227bfb99284
ms.date: 12/05/2018
ms.keywords: DeleteSubrange, DeleteSubrange method [Windows Controls], DeleteSubrange method [Windows Controls],ITextRange2 interface, ITextRange2 interface [Windows Controls],DeleteSubrange method, ITextRange2.DeleteSubrange, ITextRange2::DeleteSubrange, controls.itextrange2_deletesubrange, tom/ITextRange2::DeleteSubrange
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
 - ITextRange2::DeleteSubrange
 - tom/ITextRange2::DeleteSubrange
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
 - ITextRange2.DeleteSubrange
---

# ITextRange2::DeleteSubrange


## -description

Deletes a subrange from a range.

## -parameters

### -param cpFirst [in]

Type: <b>long</b>

The start character position of the subrange.

### -param cpLim [in]

Type: <b>long</b>

The end character position of the subrange.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>