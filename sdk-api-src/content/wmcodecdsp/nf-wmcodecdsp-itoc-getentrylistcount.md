---
UID: NF:wmcodecdsp.IToc.GetEntryListCount
title: IToc::GetEntryListCount (wmcodecdsp.h)
description: The GetEntryListCount method retrieves the number of entry lists in the table of contents.
helpviewer_keywords: ["GetEntryListCount","GetEntryListCount method [Media Foundation]","GetEntryListCount method [Media Foundation]","IToc interface","IToc interface [Media Foundation]","GetEntryListCount method","IToc.GetEntryListCount","IToc::GetEntryListCount","codecapi.itoc_getentrylistcount","mf.itoc_getentrylistcount","wmcodecdsp/IToc::GetEntryListCount"]
old-location: mf\itoc_getentrylistcount.htm
tech.root: mf
ms.assetid: 38348080-e188-4d58-8d46-dc954da398e6
ms.date: 12/05/2018
ms.keywords: GetEntryListCount, GetEntryListCount method [Media Foundation], GetEntryListCount method [Media Foundation],IToc interface, IToc interface [Media Foundation],GetEntryListCount method, IToc.GetEntryListCount, IToc::GetEntryListCount, codecapi.itoc_getentrylistcount, mf.itoc_getentrylistcount, wmcodecdsp/IToc::GetEntryListCount
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
 - IToc::GetEntryListCount
 - wmcodecdsp/IToc::GetEntryListCount
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
 - IToc.GetEntryListCount
---

# IToc::GetEntryListCount


## -description

The <b>GetEntryListCount</b> method retrieves the number of entry lists in the table of contents.

## -parameters

### -param pwCount

Pointer to a <b>WORD</b> that receives the number of entry lists.

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

<a href="/previous-versions/ee264285(v=vs.85)">GetEntryListByIndex</a>



<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc">IToc</a>