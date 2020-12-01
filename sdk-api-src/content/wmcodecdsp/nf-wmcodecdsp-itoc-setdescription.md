---
UID: NF:wmcodecdsp.IToc.SetDescription
title: IToc::SetDescription (wmcodecdsp.h)
description: The SetDescription method associates a description with the table of contents.
helpviewer_keywords: ["IToc interface [Media Foundation]","SetDescription method","IToc.SetDescription","IToc::SetDescription","SetDescription","SetDescription method [Media Foundation]","SetDescription method [Media Foundation]","IToc interface","codecapi.itoc_setdescription","mf.itoc_setdescription","wmcodecdsp/IToc::SetDescription"]
old-location: mf\itoc_setdescription.htm
tech.root: mf
ms.assetid: 718eb8bd-fdf9-434d-b859-3a38cb8fabee
ms.date: 12/05/2018
ms.keywords: IToc interface [Media Foundation],SetDescription method, IToc.SetDescription, IToc::SetDescription, SetDescription, SetDescription method [Media Foundation], SetDescription method [Media Foundation],IToc interface, codecapi.itoc_setdescription, mf.itoc_setdescription, wmcodecdsp/IToc::SetDescription
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
 - IToc::SetDescription
 - wmcodecdsp/IToc::SetDescription
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
 - IToc.SetDescription
---

# IToc::SetDescription


## -description

The <b>SetDescription</b> method associates a description with the table of contents.

## -parameters

### -param pwszDescription [in]

Pointer to a NULL-terminated, wide-character string that contains the description.

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

## -remarks

You can use this method to associate any description with the table of contents. TOC parser does not inspect or interpret the description.

## -see-also

<a href="/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-getdescription">GetDescription</a>



<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc">IToc</a>