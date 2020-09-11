---
UID: NF:msctf.ITfUIElement.GetGUID
title: ITfUIElement::GetGUID (msctf.h)
description: The ITfUIElement::GetGUID method returns the unique id of this UI element.
helpviewer_keywords: ["GetGUID","GetGUID method [Text Services Framework]","GetGUID method [Text Services Framework]","ITfUIElement interface","ITfUIElement interface [Text Services Framework]","GetGUID method","ITfUIElement.GetGUID","ITfUIElement::GetGUID","msctf/ITfUIElement::GetGUID","tsf.itfuielement_getguid"]
old-location: tsf\itfuielement_getguid.htm
tech.root: TSF
ms.assetid: 0456761e-58fc-4cda-a576-829dd2c1235f
ms.date: 12/05/2018
ms.keywords: GetGUID, GetGUID method [Text Services Framework], GetGUID method [Text Services Framework],ITfUIElement interface, ITfUIElement interface [Text Services Framework],GetGUID method, ITfUIElement.GetGUID, ITfUIElement::GetGUID, msctf/ITfUIElement::GetGUID, tsf.itfuielement_getguid
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
 - ITfUIElement::GetGUID
 - msctf/ITfUIElement::GetGUID
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
 - ITfUIElement.GetGUID
---

# ITfUIElement::GetGUID


## -description

The <b>ITfUIElement::GetGUID</b> method returns the unique id of this UI element.

## -parameters

### -param pguid [out]

[out] A pointer to receive the GUID of the UI element.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>

