---
UID: NF:imapi2.IWriteEngine2EventArgs.get_StartLba
title: IWriteEngine2EventArgs::get_StartLba (imapi2.h)
description: Retrieves the starting logical block address (LBA) of the current write operation.
helpviewer_keywords: ["IWriteEngine2EventArgs interface [IMAPI]","get_StartLba method","IWriteEngine2EventArgs.get_StartLba","IWriteEngine2EventArgs::get_StartLba","get_StartLba","get_StartLba method [IMAPI]","get_StartLba method [IMAPI]","IWriteEngine2EventArgs interface","imapi.iwriteengine2eventargs_get_startlba","imapi2/IWriteEngine2EventArgs::get_StartLba"]
old-location: imapi\iwriteengine2eventargs_get_startlba.htm
tech.root: imapi
ms.assetid: 1c2d1a1f-04b7-4453-af52-4f96e5536ad2
ms.date: 12/05/2018
ms.keywords: IWriteEngine2EventArgs interface [IMAPI],get_StartLba method, IWriteEngine2EventArgs.get_StartLba, IWriteEngine2EventArgs::get_StartLba, get_StartLba, get_StartLba method [IMAPI], get_StartLba method [IMAPI],IWriteEngine2EventArgs interface, imapi.iwriteengine2eventargs_get_startlba, imapi2/IWriteEngine2EventArgs::get_StartLba
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
 - IWriteEngine2EventArgs::get_StartLba
 - imapi2/IWriteEngine2EventArgs::get_StartLba
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
 - IWriteEngine2EventArgs.get_StartLba
---

# IWriteEngine2EventArgs::get_StartLba


## -description

Retrieves the starting logical block address (LBA) of the current write operation.

## -parameters

### -param value [out]

Starting logical block address of the write operation. Negative values for LBAs are supported.

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

## -remarks

This is the same value passed to the <a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-writesection">IWriteEngine2::WriteSection</a> method.

## -see-also

<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-writesection">IWriteEngine2::WriteSection</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs">IWriteEngine2EventArgs</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2eventargs-get_lastreadlba">IWriteEngine2EventArgs::get_LastReadLba</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2eventargs-get_lastwrittenlba">IWriteEngine2EventArgs::get_LastWrittenLba</a>