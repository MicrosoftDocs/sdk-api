---
UID: NF:wmcodecdsp.IToc.RemoveEntryListByIndex
title: IToc::RemoveEntryListByIndex (wmcodecdsp.h)
description: The RemoveEntryListByIndex method removes an entry list, specified by an index, from the table of contents.
helpviewer_keywords: ["IToc interface [Media Foundation]","RemoveEntryListByIndex method","IToc.RemoveEntryListByIndex","IToc::RemoveEntryListByIndex","RemoveEntryListByIndex","RemoveEntryListByIndex method [Media Foundation]","RemoveEntryListByIndex method [Media Foundation]","IToc interface","codecapi.itoc_removeentrylistbyindex","mf.itoc_removeentrylistbyindex","wmcodecdsp/IToc::RemoveEntryListByIndex"]
old-location: mf\itoc_removeentrylistbyindex.htm
tech.root: medfound
ms.assetid: 63137b67-dc00-48e7-88b0-2f7159c1d829
ms.date: 12/05/2018
ms.keywords: IToc interface [Media Foundation],RemoveEntryListByIndex method, IToc.RemoveEntryListByIndex, IToc::RemoveEntryListByIndex, RemoveEntryListByIndex, RemoveEntryListByIndex method [Media Foundation], RemoveEntryListByIndex method [Media Foundation],IToc interface, codecapi.itoc_removeentrylistbyindex, mf.itoc_removeentrylistbyindex, wmcodecdsp/IToc::RemoveEntryListByIndex
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
 - IToc::RemoveEntryListByIndex
 - wmcodecdsp/IToc::RemoveEntryListByIndex
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
 - IToc.RemoveEntryListByIndex
---

# IToc::RemoveEntryListByIndex


## -description

The <b>RemoveEntryListByIndex</b> method removes an entry list, specified by an index, from the table of contents.

## -parameters

### -param wEntryListIndex [in]

The index of the entry list to be removed.

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

<a href="/previous-versions/ee264281(v=vs.85)">AddEntryListByIndex</a>



<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc">IToc</a>