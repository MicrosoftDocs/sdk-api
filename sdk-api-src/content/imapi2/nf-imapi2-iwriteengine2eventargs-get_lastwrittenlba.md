---
UID: NF:imapi2.IWriteEngine2EventArgs.get_LastWrittenLba
title: IWriteEngine2EventArgs::get_LastWrittenLba (imapi2.h)
description: Retrieves the address of the sector most recently written to the device.
helpviewer_keywords: ["IWriteEngine2EventArgs interface [IMAPI]","get_LastWrittenLba method","IWriteEngine2EventArgs.get_LastWrittenLba","IWriteEngine2EventArgs::get_LastWrittenLba","get_LastWrittenLba","get_LastWrittenLba method [IMAPI]","get_LastWrittenLba method [IMAPI]","IWriteEngine2EventArgs interface","imapi.iwriteengine2eventargs_get_lastwrittenlba","imapi2/IWriteEngine2EventArgs::get_LastWrittenLba"]
old-location: imapi\iwriteengine2eventargs_get_lastwrittenlba.htm
tech.root: imapi
ms.assetid: ccb964b5-dd6f-4250-b6d2-41154258872f
ms.date: 12/05/2018
ms.keywords: IWriteEngine2EventArgs interface [IMAPI],get_LastWrittenLba method, IWriteEngine2EventArgs.get_LastWrittenLba, IWriteEngine2EventArgs::get_LastWrittenLba, get_LastWrittenLba, get_LastWrittenLba method [IMAPI], get_LastWrittenLba method [IMAPI],IWriteEngine2EventArgs interface, imapi.iwriteengine2eventargs_get_lastwrittenlba, imapi2/IWriteEngine2EventArgs::get_LastWrittenLba
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
 - IWriteEngine2EventArgs::get_LastWrittenLba
 - imapi2/IWriteEngine2EventArgs::get_LastWrittenLba
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
 - IWriteEngine2EventArgs.get_LastWrittenLba
---

# IWriteEngine2EventArgs::get_LastWrittenLba


## -description

Retrieves the address of the sector most recently written to the device.

## -parameters

### -param value [out]

Logical block address of the sector most recently written to the device.

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



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2eventargs-get_lastreadlba">IWriteEngine2EventArgs::get_LastReadLba</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2eventargs-get_startlba">IWriteEngine2EventArgs::get_StartLba</a>