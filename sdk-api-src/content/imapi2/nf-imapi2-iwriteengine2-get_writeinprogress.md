---
UID: NF:imapi2.IWriteEngine2.get_WriteInProgress
title: IWriteEngine2::get_WriteInProgress (imapi2.h)
description: Retrieves a value that indicates whether the recorder is currently writing data to the disc.
helpviewer_keywords: ["IWriteEngine2 interface [IMAPI]","get_WriteInProgress method","IWriteEngine2.get_WriteInProgress","IWriteEngine2::get_WriteInProgress","get_WriteInProgress","get_WriteInProgress method [IMAPI]","get_WriteInProgress method [IMAPI]","IWriteEngine2 interface","imapi.iwriteengine2_get_writeinprogress","imapi2/IWriteEngine2::get_WriteInProgress"]
old-location: imapi\iwriteengine2_get_writeinprogress.htm
tech.root: imapi
ms.assetid: 88f67eab-c87b-4a15-b29f-25675d0cac22
ms.date: 12/05/2018
ms.keywords: IWriteEngine2 interface [IMAPI],get_WriteInProgress method, IWriteEngine2.get_WriteInProgress, IWriteEngine2::get_WriteInProgress, get_WriteInProgress, get_WriteInProgress method [IMAPI], get_WriteInProgress method [IMAPI],IWriteEngine2 interface, imapi.iwriteengine2_get_writeinprogress, imapi2/IWriteEngine2::get_WriteInProgress
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
 - IWriteEngine2::get_WriteInProgress
 - imapi2/IWriteEngine2::get_WriteInProgress
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
 - IWriteEngine2.get_WriteInProgress
---

# IWriteEngine2::get_WriteInProgress


## -description

Retrieves a value that indicates whether the recorder is currently writing data to the disc.

## -parameters

### -param value [out]

If VARIANT_TRUE, the recorder is currently writing data to the disc. Otherwise, if VARIANT_FALSE, the recorder is not currently writing to disc.

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

<a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2">IWriteEngine2</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-cancelwrite">IWriteEngine2::CancelWrite</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-writesection">IWriteEngine2::WriteSection</a>