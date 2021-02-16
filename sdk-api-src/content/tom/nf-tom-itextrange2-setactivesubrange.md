---
UID: NF:tom.ITextRange2.SetActiveSubrange
title: ITextRange2::SetActiveSubrange (tom.h)
description: Makes the specified subrange the active subrange of this range.
helpviewer_keywords: ["ITextRange2 interface [Windows Controls]","SetActiveSubrange method","ITextRange2.SetActiveSubrange","ITextRange2::SetActiveSubrange","SetActiveSubrange","SetActiveSubrange method [Windows Controls]","SetActiveSubrange method [Windows Controls]","ITextRange2 interface","controls.itextrange2_setactivesubrange","tom/ITextRange2::SetActiveSubrange"]
old-location: controls\itextrange2_setactivesubrange.htm
tech.root: Controls
ms.assetid: a635edd3-dcb9-4f1f-bf6e-774ce3f0c505
ms.date: 12/05/2018
ms.keywords: ITextRange2 interface [Windows Controls],SetActiveSubrange method, ITextRange2.SetActiveSubrange, ITextRange2::SetActiveSubrange, SetActiveSubrange, SetActiveSubrange method [Windows Controls], SetActiveSubrange method [Windows Controls],ITextRange2 interface, controls.itextrange2_setactivesubrange, tom/ITextRange2::SetActiveSubrange
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
 - ITextRange2::SetActiveSubrange
 - tom/ITextRange2::SetActiveSubrange
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
 - ITextRange2.SetActiveSubrange
---

# ITextRange2::SetActiveSubrange


## -description

Makes the specified  subrange the active subrange of this range.

## -parameters

### -param cpAnchor [in]

Type: <b>long</b>

The anchor end character position of the subrange to make active.

### -param cpActive [in]

Type: <b>long</b>

The active end character position of the subrange to make active.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The active subrange is the one affected by operations such as Shift+Arrow keys if this range is the selection.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>