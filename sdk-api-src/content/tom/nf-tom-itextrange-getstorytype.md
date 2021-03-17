---
UID: NF:tom.ITextRange.GetStoryType
title: ITextRange::GetStoryType (tom.h)
description: Get the type of the range's story.
helpviewer_keywords: ["GetStoryType","GetStoryType method [Windows Controls]","GetStoryType method [Windows Controls]","ITextRange interface","ITextRange interface [Windows Controls]","GetStoryType method","ITextRange.GetStoryType","ITextRange::GetStoryType","_win32_ITextRange_GetStoryType","_win32_ITextRange_GetStoryType_cpp","controls.ITextRange_GetStoryType","controls._win32_ITextRange_GetStoryType","tom/ITextRange::GetStoryType"]
old-location: controls\ITextRange_GetStoryType.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getstorytype.htm
ms.date: 12/05/2018
ms.keywords: GetStoryType, GetStoryType method [Windows Controls], GetStoryType method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],GetStoryType method, ITextRange.GetStoryType, ITextRange::GetStoryType, _win32_ITextRange_GetStoryType, _win32_ITextRange_GetStoryType_cpp, controls.ITextRange_GetStoryType, controls._win32_ITextRange_GetStoryType, tom/ITextRange::GetStoryType
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
 - ITextRange::GetStoryType
 - tom/ITextRange::GetStoryType
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
 - ITextRange.GetStoryType
---

# ITextRange::GetStoryType


## -description

Get the type of the range's story.

## -parameters

### -param pValue

Type: <b>long*</b>

The type of the range's story. The <i>pValue</i> value can be one of the following values. 
					

<table class="clsStd">
<tr>
<th>Story type</th>
<th>Value</th>
<th>Story type</th>
<th>Value</th>
</tr>
<tr>
<td><b>tomUnknownStory</b></td>
<td>0</td>
<td><b>tomEvenPagesHeaderStory</b></td>
<td>6</td>
</tr>
<tr>
<td><b>tomMainTextStory</b></td>
<td>1</td>
<td><b>tomPrimaryHeaderStory</b></td>
<td>7</td>
</tr>
<tr>
<td><b>tomFootnotesStory</b></td>
<td>2</td>
<td><b>tomEvenPagesFooterStory</b></td>
<td>8</td>
</tr>
<tr>
<td><b>tomEndnotesStory</b></td>
<td>3</td>
<td><b>tomPrimaryFooterStory</b></td>
<td>9</td>
</tr>
<tr>
<td><b>tomCommentsStory</b></td>
<td>4</td>
<td><b>tomFirstPageHeaderStory</b></td>
<td>10</td>
</tr>
<tr>
<td><b>tomTextFrameStory</b></td>
<td>5</td>
<td><b>tomFirstPageFooterStory</b></td>
<td>11</td>
</tr>
</table>

## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If <i>pValue</i> is null, the method fails and it returns E_INVALIDARG.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>