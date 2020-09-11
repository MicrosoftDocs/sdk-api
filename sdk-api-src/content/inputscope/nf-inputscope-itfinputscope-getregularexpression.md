---
UID: NF:inputscope.ITfInputScope.GetRegularExpression
title: ITfInputScope::GetRegularExpression (inputscope.h)
description: ITfInputScope::GetRegularExpression method
helpviewer_keywords: ["GetRegularExpression","GetRegularExpression method [Text Services Framework]","GetRegularExpression method [Text Services Framework]","ITfInputScope interface","ITfInputScope interface [Text Services Framework]","GetRegularExpression method","ITfInputScope.GetRegularExpression","ITfInputScope::GetRegularExpression","inputscope/ITfInputScope::GetRegularExpression","tsf.itfinputscope_getregularexpression"]
old-location: tsf\itfinputscope_getregularexpression.htm
tech.root: TSF
ms.assetid: fa24c473-efc7-408f-86e8-905161de10f0
ms.date: 12/05/2018
ms.keywords: GetRegularExpression, GetRegularExpression method [Text Services Framework], GetRegularExpression method [Text Services Framework],ITfInputScope interface, ITfInputScope interface [Text Services Framework],GetRegularExpression method, ITfInputScope.GetRegularExpression, ITfInputScope::GetRegularExpression, inputscope/ITfInputScope::GetRegularExpression, tsf.itfinputscope_getregularexpression
req.header: inputscope.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: InputScope.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITfInputScope::GetRegularExpression
 - inputscope/ITfInputScope::GetRegularExpression
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
 - ITfInputScope.GetRegularExpression
---

# ITfInputScope::GetRegularExpression


## -description

Gets the regular expression string to be rssecognized.

## -parameters

### -param pbstrRegExp [out]

Pointer to a string containing the regular expression. The calling function must call <b>SystFreeString()</b> to free the memory allocated to the strings.

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
</table>

