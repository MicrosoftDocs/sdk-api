---
UID: NF:wmcodecdsp.IToc.GetContext
title: IToc::GetContext (wmcodecdsp.h)
description: The GetContext method retrieves a block of bytes that was previously associated with the table of contents by a call to SetContext.
helpviewer_keywords: ["GetContext","GetContext method [Media Foundation]","GetContext method [Media Foundation]","IToc interface","IToc interface [Media Foundation]","GetContext method","IToc.GetContext","IToc::GetContext","codecapi.itoc_getcontext","mf.itoc_getcontext","wmcodecdsp/IToc::GetContext"]
old-location: mf\itoc_getcontext.htm
tech.root: mf
ms.assetid: b4c65f1b-7465-4229-8fac-92d6b1be50da
ms.date: 12/05/2018
ms.keywords: GetContext, GetContext method [Media Foundation], GetContext method [Media Foundation],IToc interface, IToc interface [Media Foundation],GetContext method, IToc.GetContext, IToc::GetContext, codecapi.itoc_getcontext, mf.itoc_getcontext, wmcodecdsp/IToc::GetContext
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
 - IToc::GetContext
 - wmcodecdsp/IToc::GetContext
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
 - IToc.GetContext
---

# IToc::GetContext


## -description

The <b>GetContext</b> method retrieves a block of bytes that was previously associated with the table of contents by a call to <a href="/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-setcontext">SetContext</a>.

## -parameters

### -param pdwContextSize [in, out]

If <i>pbtContext</i> is <b>NULL</b>, this is an output parameter that receives the size, in bytes, of the context block. If <i>pbtContext</i> is not <b>NULL</b>, this is an input parameter that specifies the size, in bytes, of the caller-allocated buffer pointed to by <i>pbtContext</i>.

### -param pbtContext [out]

NULL, or a pointer to a caller-allocated buffer that, on successful completion, receives the context block.

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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The method returns this error code if <i>pbtContext</i> is not <b>NULL</b> and the context block is larger than the size specified by <i>bdwContextSize</i>. In that case, <i>pdwContextSize</i> serves as an output parameter and receives the size, in bytes, of the required buffer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc">IToc</a>