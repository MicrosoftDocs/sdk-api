---
UID: NF:tom.ITextRange.GetEmbeddedObject
title: ITextRange::GetEmbeddedObject (tom.h)
description: Retrieves a pointer to the embedded object at the start of the specified range, that is, at cpFirst. The range must either be an insertion point or it must select only the embedded object.
helpviewer_keywords: ["GetEmbeddedObject","GetEmbeddedObject method [Windows Controls]","GetEmbeddedObject method [Windows Controls]","ITextRange interface","ITextRange interface [Windows Controls]","GetEmbeddedObject method","ITextRange.GetEmbeddedObject","ITextRange::GetEmbeddedObject","_win32_ITextRange_GetEmbeddedObject","_win32_ITextRange_GetEmbeddedObject_cpp","controls.ITextRange_GetEmbeddedObject","controls._win32_ITextRange_GetEmbeddedObject","tom/ITextRange::GetEmbeddedObject"]
old-location: controls\ITextRange_GetEmbeddedObject.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getembeddedobject.htm
ms.date: 12/05/2018
ms.keywords: GetEmbeddedObject, GetEmbeddedObject method [Windows Controls], GetEmbeddedObject method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],GetEmbeddedObject method, ITextRange.GetEmbeddedObject, ITextRange::GetEmbeddedObject, _win32_ITextRange_GetEmbeddedObject, _win32_ITextRange_GetEmbeddedObject_cpp, controls.ITextRange_GetEmbeddedObject, controls._win32_ITextRange_GetEmbeddedObject, tom/ITextRange::GetEmbeddedObject
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
 - ITextRange::GetEmbeddedObject
 - tom/ITextRange::GetEmbeddedObject
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
 - ITextRange.GetEmbeddedObject
---

# ITextRange::GetEmbeddedObject


## -description

Retrieves a pointer to the embedded object at the start of the specified range, that is, at <i>cpFirst</i>. The range must either be an insertion point or it must select only the embedded object.

## -parameters

### -param ppObject

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>**</b>

The pointer to the object.

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
<i>ppObject</i> is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Failure for some other reason.

</td>
</tr>
</table>

## -remarks

If the start of this range does not have an embedded object or if the range selects more than a single object, <i>ppObject</i> is set equal to <b>NULL</b>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>