---
UID: NF:textstor.IAnchor.Clone
title: IAnchor::Clone (textstor.h)
description: The IAnchor::Clone method produces a new anchor object positioned at the same location, and with the same gravity, as the current anchor.
helpviewer_keywords: ["Clone","Clone method [Text Services Framework]","Clone method [Text Services Framework]","IAnchor interface","IAnchor interface [Text Services Framework]","Clone method","IAnchor.Clone","IAnchor::Clone","textstor/IAnchor::Clone","tsf.ianchor_clone"]
old-location: tsf\ianchor_clone.htm
tech.root: TSF
ms.assetid: 2c5e767a-5f66-4ecf-89f1-b27ed38e887b
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Text Services Framework], Clone method [Text Services Framework],IAnchor interface, IAnchor interface [Text Services Framework],Clone method, IAnchor.Clone, IAnchor::Clone, textstor/IAnchor::Clone, tsf.ianchor_clone
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
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
 - IAnchor::Clone
 - textstor/IAnchor::Clone
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
 - IAnchor.Clone
---

# IAnchor::Clone


## -description

The <b>IAnchor::Clone</b> method produces a new anchor object positioned at the same location, and with the same gravity, as the current anchor.

## -parameters

### -param ppaClone [out]

A new anchor object, identical to the current anchor.

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
The method failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppaClone</i> is invalid.

</td>
</tr>
</table>

## -remarks

The change history and change history masks are both cleared in the cloned anchor.

