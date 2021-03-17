---
UID: NF:imapi2.IWriteEngine2EventArgs.get_LastReadLba
title: IWriteEngine2EventArgs::get_LastReadLba (imapi2.h)
description: Retrieves the address of the sector most recently read from the burn image.
helpviewer_keywords: ["IWriteEngine2EventArgs interface [IMAPI]","get_LastReadLba method","IWriteEngine2EventArgs.get_LastReadLba","IWriteEngine2EventArgs::get_LastReadLba","get_LastReadLba","get_LastReadLba method [IMAPI]","get_LastReadLba method [IMAPI]","IWriteEngine2EventArgs interface","imapi.iwriteengine2eventargs_get_lastreadlba","imapi2/IWriteEngine2EventArgs::get_LastReadLba"]
old-location: imapi\iwriteengine2eventargs_get_lastreadlba.htm
tech.root: imapi
ms.assetid: 2db929b4-dbba-4f6a-bde0-0cefb30abf64
ms.date: 12/05/2018
ms.keywords: IWriteEngine2EventArgs interface [IMAPI],get_LastReadLba method, IWriteEngine2EventArgs.get_LastReadLba, IWriteEngine2EventArgs::get_LastReadLba, get_LastReadLba, get_LastReadLba method [IMAPI], get_LastReadLba method [IMAPI],IWriteEngine2EventArgs interface, imapi.iwriteengine2eventargs_get_lastreadlba, imapi2/IWriteEngine2EventArgs::get_LastReadLba
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
 - IWriteEngine2EventArgs::get_LastReadLba
 - imapi2/IWriteEngine2EventArgs::get_LastReadLba
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
 - IWriteEngine2EventArgs.get_LastReadLba
---

# IWriteEngine2EventArgs::get_LastReadLba


## -description

Retrieves the address of the sector most recently read from the burn image.

## -parameters

### -param value [out]

Logical block address of the sector most recently read from the input data stream.

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



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2eventargs-get_lastwrittenlba">IWriteEngine2EventArgs::get_LastWrittenLba</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2eventargs-get_startlba">IWriteEngine2EventArgs::get_StartLba</a>