---
UID: NF:wmcodecdsp.IToc.GetEntryListByIndex
title: IToc::GetEntryListByIndex (wmcodecdsp.h)
description: The GetEntryListByIndex method retrieves an entry list, specified by an index, from the table of contents.
helpviewer_keywords: ["GetEntryListByIndex","GetEntryListByIndex method [Media Foundation]","GetEntryListByIndex method [Media Foundation]","IToc interface","IToc interface [Media Foundation]","GetEntryListByIndex method","IToc.GetEntryListByIndex","IToc::GetEntryListByIndex","codecapi.itoc_getentrylistbyindex","mf.itoc_getentrylistbyindex","wmcodecdsp/IToc::GetEntryListByIndex"]
old-location: mf\itoc_getentrylistbyindex.htm
tech.root: medfound
ms.assetid: 5c457eb4-3034-40e3-93b6-e421c2e34bcf
ms.date: 12/05/2018
ms.keywords: GetEntryListByIndex, GetEntryListByIndex method [Media Foundation], GetEntryListByIndex method [Media Foundation],IToc interface, IToc interface [Media Foundation],GetEntryListByIndex method, IToc.GetEntryListByIndex, IToc::GetEntryListByIndex, codecapi.itoc_getentrylistbyindex, mf.itoc_getentrylistbyindex, wmcodecdsp/IToc::GetEntryListByIndex
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
 - IToc::GetEntryListByIndex
 - wmcodecdsp/IToc::GetEntryListByIndex
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
 - IToc.GetEntryListByIndex
---

# IToc::GetEntryListByIndex


## -description

The <b>GetEntryListByIndex</b> method retrieves an entry list, specified by an index, from the table of contents.

## -parameters

### -param wEntryListIndex [in]

The index of the entry list to retrieve.

### -param ppEntryList [out]

Pointer to a variable that receives a pointer to an <a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist">ITocEntryList</a> interface.

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