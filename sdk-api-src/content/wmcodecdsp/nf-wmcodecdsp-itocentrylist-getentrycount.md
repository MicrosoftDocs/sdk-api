---
UID: NF:wmcodecdsp.ITocEntryList.GetEntryCount
title: ITocEntryList::GetEntryCount (wmcodecdsp.h)
description: The GetEntryCount method retrieves the number of entries in the list.
helpviewer_keywords: ["GetEntryCount","GetEntryCount method [Media Foundation]","GetEntryCount method [Media Foundation]","ITocEntryList interface","ITocEntryList interface [Media Foundation]","GetEntryCount method","ITocEntryList.GetEntryCount","ITocEntryList::GetEntryCount","codecapi.itocentrylist_getentrycount","mf.itocentrylist_getentrycount","wmcodecdsp/ITocEntryList::GetEntryCount"]
old-location: mf\itocentrylist_getentrycount.htm
tech.root: mf
ms.assetid: 74c45032-578d-4ee1-a13d-f95646f27ce9
ms.date: 12/05/2018
ms.keywords: GetEntryCount, GetEntryCount method [Media Foundation], GetEntryCount method [Media Foundation],ITocEntryList interface, ITocEntryList interface [Media Foundation],GetEntryCount method, ITocEntryList.GetEntryCount, ITocEntryList::GetEntryCount, codecapi.itocentrylist_getentrycount, mf.itocentrylist_getentrycount, wmcodecdsp/ITocEntryList::GetEntryCount
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
 - ITocEntryList::GetEntryCount
 - wmcodecdsp/ITocEntryList::GetEntryCount
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
 - ITocEntryList.GetEntryCount
---

# ITocEntryList::GetEntryCount


## -description

The <b>GetEntryCount</b> method retrieves the number of entries in the list.

## -parameters

### -param pdwEntryCount [out]

Pointer to a <b>DWORD</b> that receives the number of entries.

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