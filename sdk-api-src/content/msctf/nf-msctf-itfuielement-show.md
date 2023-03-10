---
UID: NF:msctf.ITfUIElement.Show
title: ITfUIElement::Show (msctf.h)
description: The ITfUIElement::Show method shows the text service's UI of this UI element.
helpviewer_keywords: ["ITfUIElement interface [Text Services Framework]","Show method","ITfUIElement.Show","ITfUIElement::Show","Show","Show method [Text Services Framework]","Show method [Text Services Framework]","ITfUIElement interface","msctf/ITfUIElement::Show","tsf.itfuielement_show"]
old-location: tsf\itfuielement_show.htm
tech.root: TSF
ms.assetid: 423543d9-f3aa-4a42-89f6-dd1d48967c73
ms.date: 12/05/2018
ms.keywords: ITfUIElement interface [Text Services Framework],Show method, ITfUIElement.Show, ITfUIElement::Show, Show, Show method [Text Services Framework], Show method [Text Services Framework],ITfUIElement interface, msctf/ITfUIElement::Show, tsf.itfuielement_show
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfUIElement::Show
 - msctf/ITfUIElement::Show
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfUIElement.Show
---

# ITfUIElement::Show


## -description

The <b>ITfUIElement::Show</b> method shows the text service's UI of this UI element.

## -parameters

### -param bShow [in]

[in] <b>TRUE</b> to show the original UI of the element. <b>FALSE</b> to hide the original UI of the element.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>

