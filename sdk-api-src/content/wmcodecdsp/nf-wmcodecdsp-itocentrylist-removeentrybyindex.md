---
UID: NF:wmcodecdsp.ITocEntryList.RemoveEntryByIndex
title: ITocEntryList::RemoveEntryByIndex (wmcodecdsp.h)
description: The RemoveEntryByIndex method removes an entry, specified by an index, from the list.
helpviewer_keywords: ["ITocEntryList interface [Media Foundation]","RemoveEntryByIndex method","ITocEntryList.RemoveEntryByIndex","ITocEntryList::RemoveEntryByIndex","RemoveEntryByIndex","RemoveEntryByIndex method [Media Foundation]","RemoveEntryByIndex method [Media Foundation]","ITocEntryList interface","codecapi.itocentrylist_removeentrybyindex","mf.itocentrylist_removeentrybyindex","wmcodecdsp/ITocEntryList::RemoveEntryByIndex"]
old-location: mf\itocentrylist_removeentrybyindex.htm
tech.root: medfound
ms.assetid: 72b9141c-2e61-42be-a4a1-910b607ab5f1
ms.date: 12/05/2018
ms.keywords: ITocEntryList interface [Media Foundation],RemoveEntryByIndex method, ITocEntryList.RemoveEntryByIndex, ITocEntryList::RemoveEntryByIndex, RemoveEntryByIndex, RemoveEntryByIndex method [Media Foundation], RemoveEntryByIndex method [Media Foundation],ITocEntryList interface, codecapi.itocentrylist_removeentrybyindex, mf.itocentrylist_removeentrybyindex, wmcodecdsp/ITocEntryList::RemoveEntryByIndex
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
 - ITocEntryList::RemoveEntryByIndex
 - wmcodecdsp/ITocEntryList::RemoveEntryByIndex
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
 - ITocEntryList.RemoveEntryByIndex
---

# ITocEntryList::RemoveEntryByIndex


## -description

The <b>RemoveEntryByIndex</b> method removes an entry, specified by an index, from the list.

## -parameters

### -param dwEntryIndex [in]

The index of the entry to be removed.

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

<a href="/previous-versions/ee264259(v=vs.85)">AddEntryByIndex</a>



<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist">ITocEntryList</a>