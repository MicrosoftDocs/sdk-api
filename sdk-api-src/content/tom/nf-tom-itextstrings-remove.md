---
UID: NF:tom.ITextStrings.Remove
title: ITextStrings::Remove (tom.h)
description: Removes a string from a string collection, starting at an index.
helpviewer_keywords: ["ITextStrings interface [Windows Controls]","Remove method","ITextStrings.Remove","ITextStrings::Remove","Remove","Remove method [Windows Controls]","Remove method [Windows Controls]","ITextStrings interface","controls.itextstrings_remove","tom/ITextStrings::Remove"]
old-location: controls\itextstrings_remove.htm
tech.root: Controls
ms.assetid: 1909e8b6-ee18-4d17-87cf-29bb3553bb25
ms.date: 12/05/2018
ms.keywords: ITextStrings interface [Windows Controls],Remove method, ITextStrings.Remove, ITextStrings::Remove, Remove, Remove method [Windows Controls], Remove method [Windows Controls],ITextStrings interface, controls.itextstrings_remove, tom/ITextStrings::Remove
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
 - ITextStrings::Remove
 - tom/ITextStrings::Remove
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
 - ITextStrings.Remove
---

# ITextStrings::Remove


## -description

Removes a string from a string collection, starting at an index.

## -parameters

### -param iString [in]

Type: <b>long</b>

The string index.

### -param cString [in]

Type: <b>long</b>

The count of strings to remove.

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
</table>

## -remarks

The index is relative to the top of the collection, so <i>iString</i> = 0 removes the top string (<i>cString</i> must be 1), <i>iString</i> = –1 removes the one below the top string (and the top string if <i>cString</i> = 2), and so on.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextstrings">ITextStrings</a>