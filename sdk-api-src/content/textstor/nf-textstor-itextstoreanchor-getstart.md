---
UID: NF:textstor.ITextStoreAnchor.GetStart
title: ITextStoreAnchor::GetStart (textstor.h)
description: The ITextStoreAnchor::GetStart method returns an anchor positioned at the start of the text stream.
helpviewer_keywords: ["GetStart","GetStart method [Text Services Framework]","GetStart method [Text Services Framework]","ITextStoreAnchor interface","ITextStoreAnchor interface [Text Services Framework]","GetStart method","ITextStoreAnchor.GetStart","ITextStoreAnchor::GetStart","textstor/ITextStoreAnchor::GetStart","tsf.itextstoreanchor_getstart"]
old-location: tsf\itextstoreanchor_getstart.htm
tech.root: TSF
ms.assetid: 431ca3b0-920b-4a4e-b475-32175555a789
ms.date: 12/05/2018
ms.keywords: GetStart, GetStart method [Text Services Framework], GetStart method [Text Services Framework],ITextStoreAnchor interface, ITextStoreAnchor interface [Text Services Framework],GetStart method, ITextStoreAnchor.GetStart, ITextStoreAnchor::GetStart, textstor/ITextStoreAnchor::GetStart, tsf.itextstoreanchor_getstart
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - ITextStoreAnchor::GetStart
 - textstor/ITextStoreAnchor::GetStart
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
 - ITextStoreAnchor.GetStart
---

# ITextStoreAnchor::GetStart


## -description

The <b>ITextStoreAnchor::GetStart</b> method returns an anchor positioned at the start of the text stream.

## -parameters

### -param ppaStart [out]

Pointer to an anchor object located at the start of the text stream.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppaStart</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The attempt to instantiate an anchor at the start of the text stream failed.

</td>
</tr>
</table>

