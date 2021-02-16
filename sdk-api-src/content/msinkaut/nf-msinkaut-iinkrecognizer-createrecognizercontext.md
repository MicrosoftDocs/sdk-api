---
UID: NF:msinkaut.IInkRecognizer.CreateRecognizerContext
title: IInkRecognizer::CreateRecognizerContext (msinkaut.h)
description: Creates a new InkRecognizerContext object.
helpviewer_keywords: ["CreateRecognizerContext","CreateRecognizerContext method [Tablet PC]","CreateRecognizerContext method [Tablet PC]","IInkRecognizer interface","IInkRecognizer interface [Tablet PC]","CreateRecognizerContext method","IInkRecognizer.CreateRecognizerContext","IInkRecognizer::CreateRecognizerContext","b6aeec3f-8d57-4667-b171-1d8cad95f45c","msinkaut/IInkRecognizer::CreateRecognizerContext","tablet.iinkrecognizer_createrecognizercontext"]
old-location: tablet\iinkrecognizer_createrecognizercontext.htm
tech.root: tablet
ms.assetid: b6aeec3f-8d57-4667-b171-1d8cad95f45c
ms.date: 12/05/2018
ms.keywords: CreateRecognizerContext, CreateRecognizerContext method [Tablet PC], CreateRecognizerContext method [Tablet PC],IInkRecognizer interface, IInkRecognizer interface [Tablet PC],CreateRecognizerContext method, IInkRecognizer.CreateRecognizerContext, IInkRecognizer::CreateRecognizerContext, b6aeec3f-8d57-4667-b171-1d8cad95f45c, msinkaut/IInkRecognizer::CreateRecognizerContext, tablet.iinkrecognizer_createrecognizercontext
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkObj.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkRecognizer::CreateRecognizerContext
 - msinkaut/IInkRecognizer::CreateRecognizerContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkRecognizer.CreateRecognizerContext
---

# IInkRecognizer::CreateRecognizerContext


## -description

Creates a new <a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> object.

## -parameters

### -param Context [out, retval]

Returns a <a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> for the invoking <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer</a>.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contained an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer Interface</a>



<a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext Class</a>