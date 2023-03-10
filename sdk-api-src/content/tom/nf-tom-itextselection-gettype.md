---
UID: NF:tom.ITextSelection.GetType
title: ITextSelection::GetType (tom.h)
description: Gets the type of text selection.
helpviewer_keywords: ["GetType","GetType method [Windows Controls]","GetType method [Windows Controls]","ITextSelection interface","ITextSelection interface [Windows Controls]","GetType method","ITextSelection.GetType","ITextSelection::GetType","_win32_ITextSelection_GetType","_win32_ITextSelection_GetType_cpp","controls.ITextSelection_GetType","controls._win32_ITextSelection_GetType","tom/ITextSelection::GetType"]
old-location: controls\ITextSelection_GetType.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\gettype.htm
ms.date: 12/05/2018
ms.keywords: GetType, GetType method [Windows Controls], GetType method [Windows Controls],ITextSelection interface, ITextSelection interface [Windows Controls],GetType method, ITextSelection.GetType, ITextSelection::GetType, _win32_ITextSelection_GetType, _win32_ITextSelection_GetType_cpp, controls.ITextSelection_GetType, controls._win32_ITextSelection_GetType, tom/ITextSelection::GetType
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - ITextSelection::GetType
 - tom/ITextSelection::GetType
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
 - ITextSelection.GetType
---

# ITextSelection::GetType


## -description

Gets the type of text selection.

## -parameters

### -param pType

Type: <b>long*</b>

The selection type. The method returns <i>pType</i> with one of the values in the following table.


<table class="clsStd">
<tr>
<th>Selection type</th>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>tomNoSelection</b></td>
<td>0</td>
<td>No selection and no insertion point.</td>
</tr>
<tr>
<td><b>tomSelectionIP</b></td>
<td>1</td>
<td>Insertion point.</td>
</tr>
<tr>
<td><b>tomSelectionNormal</b></td>
<td>2</td>
<td>Single nondegenerate range.</td>
</tr>
<tr>
<td><b>tomSelectionFrame</b></td>
<td>3</td>
<td>Frame.</td>
</tr>
<tr>
<td><b>tomSelectionColumn</b></td>
<td>4</td>
<td>Table column.</td>
</tr>
<tr>
<td><b>tomSelectionRow</b></td>
<td>5</td>
<td>Table rows.</td>
</tr>
<tr>
<td><b>tomSelectionBlock</b></td>
<td>6</td>
<td>Block selection.</td>
</tr>
<tr>
<td><b>tomSelectionInlineShape</b></td>
<td>7</td>
<td>Picture.</td>
</tr>
<tr>
<td><b>tomSelectionShape</b></td>
<td>8</td>
<td>Shape.</td>
</tr>
</table>

## -returns

Type: <b>StdMETHODIMP</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If <i>pType</i> is null, the method fails and it returns E_INVALIDARG.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextselection">ITextSelection</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>