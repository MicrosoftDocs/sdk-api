---
UID: NF:msime.IFEDictionary.NextWords
title: IFEDictionary::NextWords (msime.h)
description: Gets the next word entry from a dictionary.
helpviewer_keywords: ["IFEDictionary interface [Internationalization for Windows Applications]","NextWords method","IFEDictionary.NextWords","IFEDictionary::NextWords","NextWords","NextWords method [Internationalization for Windows Applications]","NextWords method [Internationalization for Windows Applications]","IFEDictionary interface","intl.ifedictionary_nextwords","msime/IFEDictionary::NextWords"]
old-location: intl\ifedictionary_nextwords.htm
tech.root: Intl
ms.assetid: 551925ED-B05C-433F-91A9-D2BAC795E783
ms.date: 12/05/2018
ms.keywords: IFEDictionary interface [Internationalization for Windows Applications],NextWords method, IFEDictionary.NextWords, IFEDictionary::NextWords, NextWords, NextWords method [Internationalization for Windows Applications], NextWords method [Internationalization for Windows Applications],IFEDictionary interface, intl.ifedictionary_nextwords, msime/IFEDictionary::NextWords
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
 - IFEDictionary::NextWords
 - msime/IFEDictionary::NextWords
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
 - IFEDictionary.NextWords
---

# IFEDictionary::NextWords


## -description

Gets the next word entry from a dictionary.

This method is used only after <a href="/windows/desktop/api/msime/nf-msime-ifedictionary-getwords">GetWords</a> to get additional words.

## -parameters

### -param pchBuffer [in, out]

Buffer provided by the caller to receive the data.

### -param cbBuffer [in]

The size of <i>pchBuffer</i>.

### -param pcWrd [out]

The number of <a href="/windows/desktop/api/msime/ns-msime-imewrd">IMEWRD</a> structures returned in <i>pchBuffer</i>. If more entries are found than <i>pchBuffer</i> can store, <b>IFED_S_MORE_ENTRIES</b> will be returned.

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
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IFED_S_MORE_ENTRIES</b></dt>
</dl>
</td>
<td width="60%">
The client must call <a href="/windows/desktop/api/msime/nf-msime-ifedictionary-nextwords">NextWords</a> to get additional <a href="/windows/desktop/api/msime/ns-msime-imewrd">IMEWRD</a> structures.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msime/nf-msime-ifedictionary-getwords">GetWords</a>



<a href="/windows/desktop/api/msime/nn-msime-ifedictionary">IFEDictionary</a>



<a href="/windows/desktop/api/msime/ns-msime-imewrd">IMEWRD</a>