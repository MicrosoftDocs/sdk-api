---
UID: NF:tom.ITextStrings.Append
title: ITextStrings::Append (tom.h)
description: Appends a string to the string at the specified index in the collection.
helpviewer_keywords: ["Append","Append method [Windows Controls]","Append method [Windows Controls]","ITextStrings interface","ITextStrings interface [Windows Controls]","Append method","ITextStrings.Append","ITextStrings::Append","controls.itextstrings_append","tom/ITextStrings::Append"]
old-location: controls\itextstrings_append.htm
tech.root: Controls
ms.assetid: e280008b-b41e-43e3-9f16-6fe1f88e10ea
ms.date: 12/05/2018
ms.keywords: Append, Append method [Windows Controls], Append method [Windows Controls],ITextStrings interface, ITextStrings interface [Windows Controls],Append method, ITextStrings.Append, ITextStrings::Append, controls.itextstrings_append, tom/ITextStrings::Append
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
 - ITextStrings::Append
 - tom/ITextStrings::Append
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
 - ITextStrings.Append
---

# ITextStrings::Append


## -description

Appends a string to the string at the specified index in the collection.

## -parameters

### -param pRange [in]

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>*</b>

The string to append.

### -param iString [in]

Type: <b>long</b>

The string index.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
</table>

## -remarks

The index is relative to the top of the collection, so if  <i>iString</i> is equal to 0 the string is inserted at the top. If <i>iString</i> is equal to  –1, it is inserted below the top string, and so on.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextstrings">ITextStrings</a>