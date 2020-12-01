---
UID: NF:wmcodecdsp.ITocEntryList.GetEntryByIndex
title: ITocEntryList::GetEntryByIndex (wmcodecdsp.h)
description: The GetEntryByIndex method retrieves an entry, specified by an index, from the list.
helpviewer_keywords: ["GetEntryByIndex","GetEntryByIndex method [Media Foundation]","GetEntryByIndex method [Media Foundation]","ITocEntryList interface","ITocEntryList interface [Media Foundation]","GetEntryByIndex method","ITocEntryList.GetEntryByIndex","ITocEntryList::GetEntryByIndex","codecapi.itocentrylist_getentrybyindex","mf.itocentrylist_getentrybyindex","wmcodecdsp/ITocEntryList::GetEntryByIndex"]
old-location: mf\itocentrylist_getentrybyindex.htm
tech.root: medfound
ms.assetid: cf2171c9-67ce-4acb-97cc-af17203e815b
ms.date: 12/05/2018
ms.keywords: GetEntryByIndex, GetEntryByIndex method [Media Foundation], GetEntryByIndex method [Media Foundation],ITocEntryList interface, ITocEntryList interface [Media Foundation],GetEntryByIndex method, ITocEntryList.GetEntryByIndex, ITocEntryList::GetEntryByIndex, codecapi.itocentrylist_getentrybyindex, mf.itocentrylist_getentrybyindex, wmcodecdsp/ITocEntryList::GetEntryByIndex
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
 - ITocEntryList::GetEntryByIndex
 - wmcodecdsp/ITocEntryList::GetEntryByIndex
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
 - ITocEntryList.GetEntryByIndex
---

# ITocEntryList::GetEntryByIndex


## -description

The <b>GetEntryByIndex</b> method retrieves an entry, specified by an index, from the list.

## -parameters

### -param dwEntryIndex [in]

The index of the entry to retrieve.

### -param ppEntry [out]

Pointer to a variable that receives a pointer to an <a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry">ITocEntry</a> interface that represents the entry.

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