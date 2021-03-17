---
UID: NF:wmcodecdsp.IToc.AddEntryList
title: IToc::AddEntryList (wmcodecdsp.h)
description: The AddEntryList method adds an entry list to the table of contents and assigns an index to the entry list.
helpviewer_keywords: ["AddEntryList","AddEntryList method [Media Foundation]","AddEntryList method [Media Foundation]","IToc interface","IToc interface [Media Foundation]","AddEntryList method","IToc.AddEntryList","IToc::AddEntryList","codecapi.itoc_addentrylist","mf.itoc_addentrylist","wmcodecdsp/IToc::AddEntryList"]
old-location: mf\itoc_addentrylist.htm
tech.root: mf
ms.assetid: 8d04d6b8-d110-45a3-b3bb-5a7b680ddabe
ms.date: 12/05/2018
ms.keywords: AddEntryList, AddEntryList method [Media Foundation], AddEntryList method [Media Foundation],IToc interface, IToc interface [Media Foundation],AddEntryList method, IToc.AddEntryList, IToc::AddEntryList, codecapi.itoc_addentrylist, mf.itoc_addentrylist, wmcodecdsp/IToc::AddEntryList
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
 - IToc::AddEntryList
 - wmcodecdsp/IToc::AddEntryList
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
 - IToc.AddEntryList
---

# IToc::AddEntryList


## -description

The <b>AddEntryList</b> method adds an entry list to the table of contents and assigns an index to the entry list.

## -parameters

### -param pEntryList [in]

Pointer to an <a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist">ITocEntryList</a> interface that represents the entry list to be added.

### -param pwEntryListIndex [out]

Receives the index of the added entry list.

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

<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc">IToc</a>



<a href="/previous-versions/ee264287(v=vs.85)">RemoveEntryListByIndex</a>