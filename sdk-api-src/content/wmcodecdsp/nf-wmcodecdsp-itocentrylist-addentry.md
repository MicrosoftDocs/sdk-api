---
UID: NF:wmcodecdsp.ITocEntryList.AddEntry
title: ITocEntryList::AddEntry (wmcodecdsp.h)
description: The AddEntry method adds an individual entry to the list and assigns an index to the entry.
helpviewer_keywords: ["AddEntry","AddEntry method [Media Foundation]","AddEntry method [Media Foundation]","ITocEntryList interface","ITocEntryList interface [Media Foundation]","AddEntry method","ITocEntryList.AddEntry","ITocEntryList::AddEntry","codecapi.itocentrylist_addentry","mf.itocentrylist_addentry","wmcodecdsp/ITocEntryList::AddEntry"]
old-location: mf\itocentrylist_addentry.htm
tech.root: mf
ms.assetid: 4ac41f10-4bb5-4d50-9f7b-7c8710476162
ms.date: 12/05/2018
ms.keywords: AddEntry, AddEntry method [Media Foundation], AddEntry method [Media Foundation],ITocEntryList interface, ITocEntryList interface [Media Foundation],AddEntry method, ITocEntryList.AddEntry, ITocEntryList::AddEntry, codecapi.itocentrylist_addentry, mf.itocentrylist_addentry, wmcodecdsp/ITocEntryList::AddEntry
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
 - ITocEntryList::AddEntry
 - wmcodecdsp/ITocEntryList::AddEntry
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
 - ITocEntryList.AddEntry
---

# ITocEntryList::AddEntry


## -description

The <b>AddEntry</b> method adds an individual entry to the list and assigns an index to the entry.

## -parameters

### -param pEntry [in]

Pointer to an <a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry">ITocEntry</a> interface that represents the entry to be added.

### -param pdwEntryIndex [out]

Pointer to a <b>DWORD</b> that receives the index of the added entry.

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