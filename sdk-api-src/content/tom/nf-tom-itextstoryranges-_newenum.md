---
UID: NF:tom.ITextStoryRanges._NewEnum
title: ITextStoryRanges::_NewEnum (tom.h)
description: Retrieves an IEnumVARIANT enumerator interface for this collection of stories.
helpviewer_keywords: ["ITextStoryRanges interface [Windows Controls]","_NewEnum method","ITextStoryRanges._NewEnum","ITextStoryRanges::_NewEnum","_NewEnum","_NewEnum method [Windows Controls]","_NewEnum method [Windows Controls]","ITextStoryRanges interface","_win32_ITextStoryRanges__NewEnum","_win32_ITextStoryRanges__NewEnum_cpp","controls.ITextStoryRanges__NewEnum","controls._win32_ITextStoryRanges__NewEnum","tom/ITextStoryRanges::_NewEnum"]
old-location: controls\ITextStoryRanges__NewEnum.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\_newenum.htm
ms.date: 12/05/2018
ms.keywords: ITextStoryRanges interface [Windows Controls],_NewEnum method, ITextStoryRanges._NewEnum, ITextStoryRanges::_NewEnum, _NewEnum, _NewEnum method [Windows Controls], _NewEnum method [Windows Controls],ITextStoryRanges interface, _win32_ITextStoryRanges__NewEnum, _win32_ITextStoryRanges__NewEnum_cpp, controls.ITextStoryRanges__NewEnum, controls._win32_ITextStoryRanges__NewEnum, tom/ITextStoryRanges::_NewEnum
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
 - ITextStoryRanges::_NewEnum
 - tom/ITextStoryRanges::_NewEnum
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
 - ITextStoryRanges._NewEnum
---

# ITextStoryRanges::_NewEnum


## -description

Retrieves an 
			<b>IEnumVARIANT</b> enumerator interface for this collection of stories.

## -parameters

### -param ppunkEnum

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>**</b>

The pointer to the enumerator interface.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppunkEnum</i> is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure for some other reason.

</td>
</tr>
</table>

## -remarks

This definition together with the implementation of 
				<b>IEnumVARIANT</b>, enables one to support the following Microsoft Visual Basic for Applications (VBA) code.


```
    Dim t As ITextDocument
    Dim c As ITextStoryRanges
    Dim r As ITextRange

    Set t = gObj
    Set c = t.StoryRanges

    For Each r In c
        Debug.Print r.Text
    Next
```

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextstoryranges">ITextStoryRanges</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>