---
UID: NF:wmcodecdsp.ITocCollection.GetEntryByIndex
title: ITocCollection::GetEntryByIndex (wmcodecdsp.h)
description: The GetEntryByIndex method retrieves a table of contents, specified by an index, from the collection.
helpviewer_keywords: ["GetEntryByIndex","GetEntryByIndex method [Media Foundation]","GetEntryByIndex method [Media Foundation]","ITocCollection interface","ITocCollection interface [Media Foundation]","GetEntryByIndex method","ITocCollection.GetEntryByIndex","ITocCollection::GetEntryByIndex","codecapi.itoccollection_getentrybyindex","mf.itoccollection_getentrybyindex","wmcodecdsp/ITocCollection::GetEntryByIndex"]
old-location: mf\itoccollection_getentrybyindex.htm
tech.root: medfound
ms.assetid: 93bddd4d-8a58-46e6-9284-eaa70be2c5a4
ms.date: 12/05/2018
ms.keywords: GetEntryByIndex, GetEntryByIndex method [Media Foundation], GetEntryByIndex method [Media Foundation],ITocCollection interface, ITocCollection interface [Media Foundation],GetEntryByIndex method, ITocCollection.GetEntryByIndex, ITocCollection::GetEntryByIndex, codecapi.itoccollection_getentrybyindex, mf.itoccollection_getentrybyindex, wmcodecdsp/ITocCollection::GetEntryByIndex
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Wmvdspa.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITocCollection::GetEntryByIndex
 - wmcodecdsp/ITocCollection::GetEntryByIndex
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmvdspa.dll
api_name:
 - ITocCollection.GetEntryByIndex
---

# ITocCollection::GetEntryByIndex


## -description

The <b>GetEntryByIndex</b> method retrieves a table of contents, specified by an index, from the collection.

## -parameters

### -param dwEntryIndex [in]

Specifies the index of the table of contents to retrieve.

### -param ppToc [out]

Pointer to a variable that receives a pointer to an <a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc">IToc</a> interface that represents the table of contents.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>

## -remarks

In the context of an <a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoccollection">ITocCollection</a> interface, the word <i>entry</i> refers to an individual table of contents. That meaning of the word <i>entry</i> is in contrast to its meaning in the context of other interfaces in the TOC Parser technology. For example, in the context of an <a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc">IToc</a> interface, the word <i>entry</i> refers to a block of information, in a table of contents, that represents a section of a video file.

## -see-also

<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoccollection">ITocCollection</a>