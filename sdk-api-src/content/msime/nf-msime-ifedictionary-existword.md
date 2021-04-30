---
UID: NF:msime.IFEDictionary.ExistWord
title: IFEDictionary::ExistWord (msime.h)
description: Determines if the specified word exists in IFEDictionary.
helpviewer_keywords: ["ExistWord","ExistWord method [Internationalization for Windows Applications]","ExistWord method [Internationalization for Windows Applications]","IFEDictionary interface","IFEDictionary interface [Internationalization for Windows Applications]","ExistWord method","IFEDictionary.ExistWord","IFEDictionary::ExistWord","intl.ifedictionary_existword","msime/IFEDictionary::ExistWord"]
old-location: intl\ifedictionary_existword.htm
tech.root: Intl
ms.assetid: 70BBC94A-97D6-4237-A0C9-F6861ED6C95D
ms.date: 12/05/2018
ms.keywords: ExistWord, ExistWord method [Internationalization for Windows Applications], ExistWord method [Internationalization for Windows Applications],IFEDictionary interface, IFEDictionary interface [Internationalization for Windows Applications],ExistWord method, IFEDictionary.ExistWord, IFEDictionary::ExistWord, intl.ifedictionary_existword, msime/IFEDictionary::ExistWord
req.header: msime.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFEDictionary::ExistWord
 - msime/IFEDictionary::ExistWord
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msime.h
api_name:
 - IFEDictionary.ExistWord
---

# IFEDictionary::ExistWord


## -description

Determines if the specified word exists in <a href="/windows/desktop/api/msime/nn-msime-ifedictionary">IFEDictionary</a>.

## -parameters

### -param pwrd [in]

An <a href="/windows/desktop/api/msime/ns-msime-imewrd">IMEWRD</a> structure specifying the word to check.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The word exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The word does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msime/nn-msime-ifedictionary">IFEDictionary</a>



<a href="/windows/desktop/api/msime/ns-msime-imewrd">IMEWRD</a>