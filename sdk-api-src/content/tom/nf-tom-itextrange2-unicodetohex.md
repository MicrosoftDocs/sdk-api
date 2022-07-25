---
UID: NF:tom.ITextRange2.UnicodeToHex
title: ITextRange2::UnicodeToHex (tom.h)
description: Converts the Unicode character(s) preceding the start position of this text range to a hexadecimal number, and selects it.
helpviewer_keywords: ["ITextRange2 interface [Windows Controls]","UnicodeToHex method","ITextRange2.UnicodeToHex","ITextRange2::UnicodeToHex","UnicodeToHex","UnicodeToHex method [Windows Controls]","UnicodeToHex method [Windows Controls]","ITextRange2 interface","controls.itextrange2_unicodetohex","tom/ITextRange2::UnicodeToHex"]
old-location: controls\itextrange2_unicodetohex.htm
tech.root: Controls
ms.assetid: 538f7db4-0739-421c-9d51-8144b2d52334
ms.date: 12/05/2018
ms.keywords: ITextRange2 interface [Windows Controls],UnicodeToHex method, ITextRange2.UnicodeToHex, ITextRange2::UnicodeToHex, UnicodeToHex, UnicodeToHex method [Windows Controls], UnicodeToHex method [Windows Controls],ITextRange2 interface, controls.itextrange2_unicodetohex, tom/ITextRange2::UnicodeToHex
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
 - ITextRange2::UnicodeToHex
 - tom/ITextRange2::UnicodeToHex
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
 - ITextRange2.UnicodeToHex
---

# ITextRange2::UnicodeToHex


## -description

Converts the Unicode character(s) preceding the start position of this text range to a hexadecimal number, and selects it.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Some Unicode surrogates for hex values from 0x10000 up to 0x10FFFF are for internal use: <table>
<tr>
<th>Hex values</th>
<th>Available for use</th>
</tr>
<tr>
<td> 0xFDD0 – 0xFDEF, 0xFFF9-0xFFFF</td>
<td>Internal use only</td>
</tr>
<tr>
<td>0xA – 0xD in the C0 range (0-0x1F)</td>
<td>Available for use</td>
</tr>
<tr>
<td>C1 range (0x80 – 0x9F)</td>
<td>Internal use only</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>
