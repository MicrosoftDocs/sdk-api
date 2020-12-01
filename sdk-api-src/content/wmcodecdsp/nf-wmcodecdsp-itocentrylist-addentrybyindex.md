---
UID: NF:wmcodecdsp.ITocEntryList.AddEntryByIndex
title: ITocEntryList::AddEntryByIndex (wmcodecdsp.h)
description: The AddEntryByIndex method adds an individual entry to the list and associates a caller-supplied index with the entry.
helpviewer_keywords: ["AddEntryByIndex","AddEntryByIndex method [Media Foundation]","AddEntryByIndex method [Media Foundation]","ITocEntryList interface","ITocEntryList interface [Media Foundation]","AddEntryByIndex method","ITocEntryList.AddEntryByIndex","ITocEntryList::AddEntryByIndex","codecapi.itocentrylist_addentrybyindex","mf.itocentrylist_addentrybyindex","wmcodecdsp/ITocEntryList::AddEntryByIndex"]
old-location: mf\itocentrylist_addentrybyindex.htm
tech.root: medfound
ms.assetid: c8146c0f-ac91-42c7-9368-dd2db6079d3d
ms.date: 12/05/2018
ms.keywords: AddEntryByIndex, AddEntryByIndex method [Media Foundation], AddEntryByIndex method [Media Foundation],ITocEntryList interface, ITocEntryList interface [Media Foundation],AddEntryByIndex method, ITocEntryList.AddEntryByIndex, ITocEntryList::AddEntryByIndex, codecapi.itocentrylist_addentrybyindex, mf.itocentrylist_addentrybyindex, wmcodecdsp/ITocEntryList::AddEntryByIndex
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
 - ITocEntryList::AddEntryByIndex
 - wmcodecdsp/ITocEntryList::AddEntryByIndex
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
 - ITocEntryList.AddEntryByIndex
---

# ITocEntryList::AddEntryByIndex


## -description

The <b>AddEntryByIndex</b> method adds an individual entry to the list and associates a caller-supplied index with the entry.

## -parameters

### -param dwEntryIndex [in]

The index of the entry to be added.

### -param pEntry [in]

Pointer to an <a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry">ITocEntry</a> interface that represents the entry to be added.

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

## -see-also

<a href="/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-getentrybyindex">GetEntryByIndex</a>



<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist">ITocEntryList</a>