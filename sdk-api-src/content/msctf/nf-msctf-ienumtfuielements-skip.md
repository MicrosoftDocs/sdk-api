---
UID: NF:msctf.IEnumTfUIElements.Skip
title: IEnumTfUIElements::Skip (msctf.h)
description: The IEnumTfUIElements::Skip method obtains, from the current position, the specified number of elements in the enumeration sequence.
helpviewer_keywords: ["IEnumTfUIElements interface [Text Services Framework]","Skip method","IEnumTfUIElements.Skip","IEnumTfUIElements::Skip","Skip","Skip method [Text Services Framework]","Skip method [Text Services Framework]","IEnumTfUIElements interface","msctf/IEnumTfUIElements::Skip","tsf.ienumtfuielements_skip"]
old-location: tsf\ienumtfuielements_skip.htm
tech.root: TSF
ms.assetid: 44ba8fb1-e702-4f53-b95a-719b4fdfcaa0
ms.date: 12/05/2018
ms.keywords: IEnumTfUIElements interface [Text Services Framework],Skip method, IEnumTfUIElements.Skip, IEnumTfUIElements::Skip, Skip, Skip method [Text Services Framework], Skip method [Text Services Framework],IEnumTfUIElements interface, msctf/IEnumTfUIElements::Skip, tsf.ienumtfuielements_skip
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
 - IEnumTfUIElements::Skip
 - msctf/IEnumTfUIElements::Skip
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
 - IEnumTfUIElements.Skip
---

# IEnumTfUIElements::Skip


## -description

The <b>IEnumTfUIElements::Skip</b> method obtains, from the current position, the specified number of elements in the enumeration sequence.

## -parameters

### -param ulCount [in]

[in] Specifies the number of elements to skip.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method reached the end of the enumeration before the specified number of elements could be skipped.

</td>
</tr>
</table>

