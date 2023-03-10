---
UID: NF:tom.ITextStrings.Add
title: ITextStrings::Add (tom.h)
description: Adds a string to the end of the collection.
helpviewer_keywords: ["Add","Add method [Windows Controls]","Add method [Windows Controls]","ITextStrings interface","ITextStrings interface [Windows Controls]","Add method","ITextStrings.Add","ITextStrings::Add","controls.itextstrings_add","tom/ITextStrings::Add"]
old-location: controls\itextstrings_add.htm
tech.root: Controls
ms.assetid: 59630068-e3c7-4c3b-bd89-f1127759f979
ms.date: 12/05/2018
ms.keywords: Add, Add method [Windows Controls], Add method [Windows Controls],ITextStrings interface, ITextStrings interface [Windows Controls],Add method, ITextStrings.Add, ITextStrings::Add, controls.itextstrings_add, tom/ITextStrings::Add
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
 - ITextStrings::Add
 - tom/ITextStrings::Add
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
 - ITextStrings.Add
---

# ITextStrings::Add


## -description

Adds a string to the end of the collection.

## -parameters

### -param bstr [in]

Type: <b>BSTR</b>

The string. The value can be <b>NULL</b> for  a null string.

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

Adding an item to the end of a collection is like pushing a parameter onto the stack.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextstrings">ITextStrings</a>