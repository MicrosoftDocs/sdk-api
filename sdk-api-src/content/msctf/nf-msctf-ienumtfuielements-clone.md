---
UID: NF:msctf.IEnumTfUIElements.Clone
title: IEnumTfUIElements::Clone (msctf.h)
description: The IEnumTfUIElements::Clone method creates a copy of the enumerator object.
helpviewer_keywords: ["Clone","Clone method [Text Services Framework]","Clone method [Text Services Framework]","IEnumTfUIElements interface","IEnumTfUIElements interface [Text Services Framework]","Clone method","IEnumTfUIElements.Clone","IEnumTfUIElements::Clone","msctf/IEnumTfUIElements::Clone","tsf.ienumtfuielements_clone"]
old-location: tsf\ienumtfuielements_clone.htm
tech.root: TSF
ms.assetid: 3949ea4d-9360-4524-9495-31a884cac309
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Text Services Framework], Clone method [Text Services Framework],IEnumTfUIElements interface, IEnumTfUIElements interface [Text Services Framework],Clone method, IEnumTfUIElements.Clone, IEnumTfUIElements::Clone, msctf/IEnumTfUIElements::Clone, tsf.ienumtfuielements_clone
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
 - IEnumTfUIElements::Clone
 - msctf/IEnumTfUIElements::Clone
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
 - IEnumTfUIElements.Clone
---

# IEnumTfUIElements::Clone


## -description

The <b>IEnumTfUIElements::Clone</b> method creates a copy of the enumerator object.

## -parameters

### -param ppEnum [out]

[out] A pointer to a <a href="/windows/desktop/api/msctf/nn-msctf-ienumtfuielements">IEnumTfUIElements</a> interface.

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