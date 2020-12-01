---
UID: NF:wmcodecdsp.IToc.SetContext
title: IToc::SetContext (wmcodecdsp.h)
description: The SetContext method associates a caller-supplied context block with the table of contents.
helpviewer_keywords: ["IToc interface [Media Foundation]","SetContext method","IToc.SetContext","IToc::SetContext","SetContext","SetContext method [Media Foundation]","SetContext method [Media Foundation]","IToc interface","codecapi.itoc_setcontext","mf.itoc_setcontext","wmcodecdsp/IToc::SetContext"]
old-location: mf\itoc_setcontext.htm
tech.root: mf
ms.assetid: 45aadac5-6c65-4525-a1fc-b045337a6030
ms.date: 12/05/2018
ms.keywords: IToc interface [Media Foundation],SetContext method, IToc.SetContext, IToc::SetContext, SetContext, SetContext method [Media Foundation], SetContext method [Media Foundation],IToc interface, codecapi.itoc_setcontext, mf.itoc_setcontext, wmcodecdsp/IToc::SetContext
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
 - IToc::SetContext
 - wmcodecdsp/IToc::SetContext
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
 - IToc.SetContext
---

# IToc::SetContext


## -description

The <b>SetContext</b> method associates a caller-supplied context block with the table of contents.

## -parameters

### -param dwContextSize [in]

The size, in bytes, of the context block.

### -param pbtContext [in]

Pointer to the first byte of the context block.

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

You can use this method to associate any information with the table of contents. The type of information you store in the context block is completely up to you. TOC Parser does not inspect or interpret the context block.

## -see-also

<a href="/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-getcontext">GetContext</a>



<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc">IToc</a>