---
UID: NF:wmcodecdsp.ITocEntry.SetTitle
title: ITocEntry::SetTitle (wmcodecdsp.h)
description: The SetTitle method sets the title of the entry.
helpviewer_keywords: ["ITocEntry interface [Media Foundation]","SetTitle method","ITocEntry.SetTitle","ITocEntry::SetTitle","SetTitle","SetTitle method [Media Foundation]","SetTitle method [Media Foundation]","ITocEntry interface","codecapi.itocentry_settitle","mf.itocentry_settitle","wmcodecdsp/ITocEntry::SetTitle"]
old-location: mf\itocentry_settitle.htm
tech.root: mf
ms.assetid: 24ab6c56-59ae-4fdf-b18e-75f616ee5a80
ms.date: 12/05/2018
ms.keywords: ITocEntry interface [Media Foundation],SetTitle method, ITocEntry.SetTitle, ITocEntry::SetTitle, SetTitle, SetTitle method [Media Foundation], SetTitle method [Media Foundation],ITocEntry interface, codecapi.itocentry_settitle, mf.itocentry_settitle, wmcodecdsp/ITocEntry::SetTitle
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
 - ITocEntry::SetTitle
 - wmcodecdsp/ITocEntry::SetTitle
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
 - ITocEntry.SetTitle
---

# ITocEntry::SetTitle


## -description

The <b>SetTitle</b> method sets the title of the entry.

## -parameters

### -param pwszTitle [in]

Pointer to a NULL-terminated wide-character string that contains the title.

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

<a href="/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-gettitle">GetTitle</a>



<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry">ITocEntry</a>