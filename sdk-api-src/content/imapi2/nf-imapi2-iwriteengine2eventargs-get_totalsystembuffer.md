---
UID: NF:imapi2.IWriteEngine2EventArgs.get_TotalSystemBuffer
title: IWriteEngine2EventArgs::get_TotalSystemBuffer (imapi2.h)
description: Retrieves the size of the internal data buffer that is used for writing to disc.
helpviewer_keywords: ["IWriteEngine2EventArgs interface [IMAPI]","get_TotalSystemBuffer method","IWriteEngine2EventArgs.get_TotalSystemBuffer","IWriteEngine2EventArgs::get_TotalSystemBuffer","get_TotalSystemBuffer","get_TotalSystemBuffer method [IMAPI]","get_TotalSystemBuffer method [IMAPI]","IWriteEngine2EventArgs interface","imapi.iwriteengine2eventargs_get_totalsystembuffer","imapi2/IWriteEngine2EventArgs::get_TotalSystemBuffer"]
old-location: imapi\iwriteengine2eventargs_get_totalsystembuffer.htm
tech.root: imapi
ms.assetid: dfdf4116-0402-4c90-8b9b-0758fd0bb973
ms.date: 12/05/2018
ms.keywords: IWriteEngine2EventArgs interface [IMAPI],get_TotalSystemBuffer method, IWriteEngine2EventArgs.get_TotalSystemBuffer, IWriteEngine2EventArgs::get_TotalSystemBuffer, get_TotalSystemBuffer, get_TotalSystemBuffer method [IMAPI], get_TotalSystemBuffer method [IMAPI],IWriteEngine2EventArgs interface, imapi.iwriteengine2eventargs_get_totalsystembuffer, imapi2/IWriteEngine2EventArgs::get_TotalSystemBuffer
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWriteEngine2EventArgs::get_TotalSystemBuffer
 - imapi2/IWriteEngine2EventArgs::get_TotalSystemBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IWriteEngine2EventArgs.get_TotalSystemBuffer
---

# IWriteEngine2EventArgs::get_TotalSystemBuffer


## -description

Retrieves the size of the internal data buffer that is used for writing to disc.

## -parameters

### -param value [out]

Size, in bytes, of the internal data buffer that is used for writing to disc.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs">IWriteEngine2EventArgs</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2eventargs-get_freesystembuffer">IWriteEngine2EventArgs::get_FreeSystemBuffer</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2eventargs-get_usedsystembuffer">IWriteEngine2EventArgs::get_UsedSystemBuffer</a>