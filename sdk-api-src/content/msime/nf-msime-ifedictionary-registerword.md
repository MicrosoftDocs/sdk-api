---
UID: NF:msime.IFEDictionary.RegisterWord
title: IFEDictionary::RegisterWord (msime.h)
description: Registers a new word or deletes an existing word in the IFEDictionary.
helpviewer_keywords: ["IFED_REG_DEL","IFED_REG_HEAD","IFED_REG_TAIL","IFEDictionary interface [Internationalization for Windows Applications]","RegisterWord method","IFEDictionary.RegisterWord","IFEDictionary::RegisterWord","RegisterWord","RegisterWord method [Internationalization for Windows Applications]","RegisterWord method [Internationalization for Windows Applications]","IFEDictionary interface","intl.ifedictionary_registerword","msime/IFEDictionary::RegisterWord"]
old-location: intl\ifedictionary_registerword.htm
tech.root: Intl
ms.assetid: CD79FBF5-E540-4B5C-A398-B7FE95F86701
ms.date: 12/05/2018
ms.keywords: IFED_REG_DEL, IFED_REG_HEAD, IFED_REG_TAIL, IFEDictionary interface [Internationalization for Windows Applications],RegisterWord method, IFEDictionary.RegisterWord, IFEDictionary::RegisterWord, RegisterWord, RegisterWord method [Internationalization for Windows Applications], RegisterWord method [Internationalization for Windows Applications],IFEDictionary interface, intl.ifedictionary_registerword, msime/IFEDictionary::RegisterWord
req.header: msime.h
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFEDictionary::RegisterWord
 - msime/IFEDictionary::RegisterWord
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
 - IFEDictionary.RegisterWord
---

# IFEDictionary::RegisterWord


## -description

Registers a new word or deletes an existing word in the <a href="/windows/desktop/api/msime/nn-msime-ifedictionary">IFEDictionary</a>.

## -parameters

### -param reg [in]

Type of operation to perform. This can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IFED_REG_HEAD"></a><a id="ifed_reg_head"></a><dl>
<dt><b>IFED_REG_HEAD</b></dt>
</dl>
</td>
<td width="60%">
Register the word at the head of the dictionary.

</td>
</tr>
<tr>
<td width="40%"><a id="IFED_REG_TAIL"></a><a id="ifed_reg_tail"></a><dl>
<dt><b>IFED_REG_TAIL</b></dt>
</dl>
</td>
<td width="60%">
Register the word at the tail of the dictionary.

</td>
</tr>
<tr>
<td width="40%"><a id="IFED_REG_DEL"></a><a id="ifed_reg_del"></a><dl>
<dt><b>IFED_REG_DEL</b></dt>
</dl>
</td>
<td width="60%">
Delete the word from the dictionary.

</td>
</tr>
</table>

### -param pwrd [in]

An <a href="/windows/desktop/api/msime/ns-msime-imewrd">IMEWRD</a> structure specifying the word to register or delete.

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
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IFED_E_NOT_USER_DIC</b></dt>
</dl>
</td>
<td width="60%">
This <a href="/windows/desktop/api/msime/nn-msime-ifedictionary">IFEDictionary</a> object is not a user dictionary.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IFED_S_WORD_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The word is already registered.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IFED_E_USER_COMMENT</b></dt>
</dl>
</td>
<td width="60%">
Failed to insert the user comment.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Failed to register or delete the word.

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