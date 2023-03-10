---
UID: NF:tom.ITextStrings.PrefixTop
title: ITextStrings::PrefixTop (tom.h)
description: Prefixes a string to the top string in the collection.
helpviewer_keywords: ["ITextStrings interface [Windows Controls]","PrefixTop method","ITextStrings.PrefixTop","ITextStrings::PrefixTop","PrefixTop","PrefixTop method [Windows Controls]","PrefixTop method [Windows Controls]","ITextStrings interface","controls.itextstrings_prefixtop","tom/ITextStrings::PrefixTop"]
old-location: controls\itextstrings_prefixtop.htm
tech.root: Controls
ms.assetid: fbdae612-1d6e-4f10-9b55-5ee038f27b79
ms.date: 12/05/2018
ms.keywords: ITextStrings interface [Windows Controls],PrefixTop method, ITextStrings.PrefixTop, ITextStrings::PrefixTop, PrefixTop, PrefixTop method [Windows Controls], PrefixTop method [Windows Controls],ITextStrings interface, controls.itextstrings_prefixtop, tom/ITextStrings::PrefixTop
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
 - ITextStrings::PrefixTop
 - tom/ITextStrings::PrefixTop
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
 - ITextStrings.PrefixTop
---

# ITextStrings::PrefixTop


## -description

Prefixes a string to the top  string in the collection.

## -parameters

### -param bstr [in]

Type: <b>BSTR</b>

The string to prefix to the collection.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextstrings">ITextStrings</a>