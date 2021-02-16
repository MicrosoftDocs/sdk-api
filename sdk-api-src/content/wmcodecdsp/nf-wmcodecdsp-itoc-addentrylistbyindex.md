---
UID: NF:wmcodecdsp.IToc.AddEntryListByIndex
title: IToc::AddEntryListByIndex (wmcodecdsp.h)
description: The AddEntryListByIndex method adds an entry list to the table of contents and associates a caller-supplied index with the entry list.
helpviewer_keywords: ["AddEntryListByIndex","AddEntryListByIndex method [Media Foundation]","AddEntryListByIndex method [Media Foundation]","IToc interface","IToc interface [Media Foundation]","AddEntryListByIndex method","IToc.AddEntryListByIndex","IToc::AddEntryListByIndex","codecapi.itoc_addentrylistbyindex","mf.itoc_addentrylistbyindex","wmcodecdsp/IToc::AddEntryListByIndex"]
old-location: mf\itoc_addentrylistbyindex.htm
tech.root: medfound
ms.assetid: 273e1c38-7f1a-4f04-b1a8-ba27b5babf94
ms.date: 12/05/2018
ms.keywords: AddEntryListByIndex, AddEntryListByIndex method [Media Foundation], AddEntryListByIndex method [Media Foundation],IToc interface, IToc interface [Media Foundation],AddEntryListByIndex method, IToc.AddEntryListByIndex, IToc::AddEntryListByIndex, codecapi.itoc_addentrylistbyindex, mf.itoc_addentrylistbyindex, wmcodecdsp/IToc::AddEntryListByIndex
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
 - IToc::AddEntryListByIndex
 - wmcodecdsp/IToc::AddEntryListByIndex
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
 - IToc.AddEntryListByIndex
---

# IToc::AddEntryListByIndex


## -description

The <b>AddEntryListByIndex</b> method adds an entry list to the table of contents and associates a caller-supplied index with the entry list.

## -parameters

### -param wEntryListIndex [in]

The index, specified by the caller, to be associated with the entry list.

### -param pEntryList [in]

Pointer to an <a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist">ITocEntryList</a> interface that represents the entry list to be added.

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