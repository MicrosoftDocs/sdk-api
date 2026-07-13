---
UID: NF:wmcodecdsp.ITocCollection.AddEntryByIndex
title: ITocCollection::AddEntryByIndex (wmcodecdsp.h)
description: The AddEntryByIndex adds an individual table of contents to the collection and associates a caller-supplied index with the table of contents.
helpviewer_keywords: ["AddEntryByIndex","AddEntryByIndex method [Media Foundation]","AddEntryByIndex method [Media Foundation]","ITocCollection interface","ITocCollection interface [Media Foundation]","AddEntryByIndex method","ITocCollection.AddEntryByIndex","ITocCollection::AddEntryByIndex","codecapi.itoccollection_addentrybyindex","mf.itoccollection_addentrybyindex","wmcodecdsp/ITocCollection::AddEntryByIndex"]
old-location: mf\itoccollection_addentrybyindex.htm
tech.root: medfound
ms.assetid: 61f3103b-9b81-4729-a410-ab5ea63e072c
ms.date: 12/05/2018
ms.keywords: AddEntryByIndex, AddEntryByIndex method [Media Foundation], AddEntryByIndex method [Media Foundation],ITocCollection interface, ITocCollection interface [Media Foundation],AddEntryByIndex method, ITocCollection.AddEntryByIndex, ITocCollection::AddEntryByIndex, codecapi.itoccollection_addentrybyindex, mf.itoccollection_addentrybyindex, wmcodecdsp/ITocCollection::AddEntryByIndex
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
 - ITocCollection::AddEntryByIndex
 - wmcodecdsp/ITocCollection::AddEntryByIndex
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
 - ITocCollection.AddEntryByIndex
---

# ITocCollection::AddEntryByIndex


## -description

The <b>AddEntryByIndex</b> adds an individual table of contents to the collection and associates a caller-supplied index with the table of contents.

## -parameters

### -param dwEntryIndex [in]

The index, specified by the caller, to be associated with the table of contents.

### -param pToc [in]

Pointer to an <a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc">IToc</a> interface that represents the table of contents to be added.

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

<a href="/previous-versions/ee264253(v=vs.85)">GetEntryByIndex</a>



<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoccollection">ITocCollection</a>