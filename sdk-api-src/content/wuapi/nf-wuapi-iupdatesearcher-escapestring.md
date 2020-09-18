---
UID: NF:wuapi.IUpdateSearcher.EscapeString
title: IUpdateSearcher::EscapeString (wuapi.h)
description: Converts a string into a string that can be used as a literal value in a search criteria string.
helpviewer_keywords: ["EscapeString","EscapeString method [Windows Update Agent]","EscapeString method [Windows Update Agent]","IUpdateSearcher interface","IUpdateSearcher interface [Windows Update Agent]","EscapeString method","IUpdateSearcher.EscapeString","IUpdateSearcher::EscapeString","wua.iupdatesearcherescapestring","wuapi/IUpdateSearcher::EscapeString"]
old-location: wua\iupdatesearcherescapestring.htm
tech.root: wua
ms.assetid: 27d510da-3d0c-4a8a-89c9-4abc009489b4
ms.date: 12/05/2018
ms.keywords: EscapeString, EscapeString method [Windows Update Agent], EscapeString method [Windows Update Agent],IUpdateSearcher interface, IUpdateSearcher interface [Windows Update Agent],EscapeString method, IUpdateSearcher.EscapeString, IUpdateSearcher::EscapeString, wua.iupdatesearcherescapestring, wuapi/IUpdateSearcher::EscapeString
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUpdateSearcher::EscapeString
 - wuapi/IUpdateSearcher::EscapeString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateSearcher.EscapeString
---

# IUpdateSearcher::EscapeString


## -description

Converts a string into a string that can be used as a literal value in a search criteria string.

## -parameters

### -param unescaped [in]

A string to be escaped.

### -param retval [out]

The resulting escaped string.

## -returns

Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code. 

This method can also return the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter value is invalid or <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesearcher">IUpdateSearcher</a>