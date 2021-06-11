---
UID: NF:msinkaut.IInkRecognizerContext.IsStringSupported
title: IInkRecognizerContext::IsStringSupported (msinkaut.h)
description: Indicates whether the system dictionary, user dictionary, or word list contain a specified string.
helpviewer_keywords: ["5344044a-0973-4ab2-bf5c-74e0d07d4e76","IInkRecognizerContext interface [Tablet PC]","IsStringSupported method","IInkRecognizerContext.IsStringSupported","IInkRecognizerContext::IsStringSupported","IsStringSupported","IsStringSupported method [Tablet PC]","IsStringSupported method [Tablet PC]","IInkRecognizerContext interface","msinkaut/IInkRecognizerContext::IsStringSupported","tablet.inkrecognizercontext_isstringsupported"]
old-location: tablet\inkrecognizercontext_isstringsupported.htm
tech.root: tablet
ms.assetid: 5344044a-0973-4ab2-bf5c-74e0d07d4e76
ms.date: 12/05/2018
ms.keywords: 5344044a-0973-4ab2-bf5c-74e0d07d4e76, IInkRecognizerContext interface [Tablet PC],IsStringSupported method, IInkRecognizerContext.IsStringSupported, IInkRecognizerContext::IsStringSupported, IsStringSupported, IsStringSupported method [Tablet PC], IsStringSupported method [Tablet PC],IInkRecognizerContext interface, msinkaut/IInkRecognizerContext::IsStringSupported, tablet.inkrecognizercontext_isstringsupported
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
 - IInkRecognizerContext::IsStringSupported
 - msinkaut/IInkRecognizerContext::IsStringSupported
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
 - IInkRecognizerContext.IsStringSupported
---

# IInkRecognizerContext::IsStringSupported


## -description

Indicates whether the system dictionary, user dictionary, or <a href="/windows/desktop/tablet/inkwordlist-class">word list</a> contain a specified string.

## -parameters

### -param String [in]

The string to look up in the dictionaries and word list.

For more information about the BSTR data type, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

### -param Supported [out, retval]

When this method returns, contains <b>VARIANT_TRUE</b> if the string is in the dictionary or word list; otherwise <b>VARIANT_FALSE</b>.

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
One of the dictionaries contains the string.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid input string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred while processing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Cannot allocate memory operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected parameter or property type.

</td>
</tr>
</table>

## -remarks

This method considers all flags and factoid, among other things, that give context to the string that is being tested.

This method does not search the user dictionary if you specify a <a href="/windows/desktop/tablet/inkwordlist-class">word list</a> for the context. The recognizer uses the speech dictionary in Microsoft Office XP.

Use the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid">Factoid</a> property to limit the search to the system dictionary or the word list that is associated with the context. For example, to limit the search to the system dictionary, specify the <a href="/windows/desktop/tablet/factoid-constants">SystemDictionary</a> factoid. To improve the results, you may also need to set the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags">RecognitionFlags</a> property.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid">Factoid Property [InkRecognizeContext Class]</a>



<a href="../msinkaut/nn-msinkaut-iinkrecognizercontext.md">IInkRecognizerContext</a>



<a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext Class</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags">RecognitionFlags Property</a>
