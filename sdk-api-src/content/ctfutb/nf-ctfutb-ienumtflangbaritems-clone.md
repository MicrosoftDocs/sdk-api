---
UID: NF:ctfutb.IEnumTfLangBarItems.Clone
title: IEnumTfLangBarItems::Clone (ctfutb.h)
description: IEnumTfLangBarItems::Clone method
helpviewer_keywords: ["Clone","Clone method [Text Services Framework]","Clone method [Text Services Framework]","IEnumTfLangBarItems interface","IEnumTfLangBarItems interface [Text Services Framework]","Clone method","IEnumTfLangBarItems.Clone","IEnumTfLangBarItems::Clone","_tsf_ienumtflangbaritems_clone_ref","ctfutb/IEnumTfLangBarItems::Clone","tsf.ienumtflangbaritems_clone"]
old-location: tsf\ienumtflangbaritems_clone.htm
tech.root: TSF
ms.assetid: 2a1f4a40-cf2c-4872-bb15-c4622ab2bfd1
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Text Services Framework], Clone method [Text Services Framework],IEnumTfLangBarItems interface, IEnumTfLangBarItems interface [Text Services Framework],Clone method, IEnumTfLangBarItems.Clone, IEnumTfLangBarItems::Clone, _tsf_ienumtflangbaritems_clone_ref, ctfutb/IEnumTfLangBarItems::Clone, tsf.ienumtflangbaritems_clone
req.header: ctfutb.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctfutb.idl
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
 - IEnumTfLangBarItems::Clone
 - ctfutb/IEnumTfLangBarItems::Clone
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - IEnumTfLangBarItems.Clone
---

# IEnumTfLangBarItems::Clone


## -description

Creates a copy of the enumerator object.

## -parameters

### -param ppEnum [out]

Pointer to an <a href="/windows/desktop/api/ctfutb/nn-ctfutb-ienumtflangbaritems">IEnumTfLangBarItems</a> interface pointer that receives the new enumerator.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ctfutb/nn-ctfutb-ienumtflangbaritems">IEnumTfLangBarItems
      </a>