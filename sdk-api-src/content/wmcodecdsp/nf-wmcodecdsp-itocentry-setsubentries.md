---
UID: NF:wmcodecdsp.ITocEntry.SetSubEntries
title: ITocEntry::SetSubEntries (wmcodecdsp.h)
description: The SetSubEntries identifies a set of entries as being subentries of this entry.
helpviewer_keywords: ["ITocEntry interface [Media Foundation]","SetSubEntries method","ITocEntry.SetSubEntries","ITocEntry::SetSubEntries","SetSubEntries","SetSubEntries method [Media Foundation]","SetSubEntries method [Media Foundation]","ITocEntry interface","codecapi.itocentry_setsubentries","mf.itocentry_setsubentries","wmcodecdsp/ITocEntry::SetSubEntries"]
old-location: mf\itocentry_setsubentries.htm
tech.root: mf
ms.assetid: 4b3f4038-483c-4f00-a819-ace83d99da58
ms.date: 12/05/2018
ms.keywords: ITocEntry interface [Media Foundation],SetSubEntries method, ITocEntry.SetSubEntries, ITocEntry::SetSubEntries, SetSubEntries, SetSubEntries method [Media Foundation], SetSubEntries method [Media Foundation],ITocEntry interface, codecapi.itocentry_setsubentries, mf.itocentry_setsubentries, wmcodecdsp/ITocEntry::SetSubEntries
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
 - ITocEntry::SetSubEntries
 - wmcodecdsp/ITocEntry::SetSubEntries
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
 - ITocEntry.SetSubEntries
---

# ITocEntry::SetSubEntries


## -description

The <b>SetSubEntries</b> identifies a set of entries as being subentries of this entry.

## -parameters

### -param dwNumSubEntries [in]

The number of indices in the array pointed to by <i>pwSubEntryIndices</i>.

### -param pwSubEntryIndices [in]

Pointer to an array of <b>WORD</b>s. Each <b>WORD</b> in the array specifies the index of an entry that is to be considered a subentry of this entry.

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

<a href="/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-getsubentries">GetSubEntries</a>



<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry">ITocEntry</a>