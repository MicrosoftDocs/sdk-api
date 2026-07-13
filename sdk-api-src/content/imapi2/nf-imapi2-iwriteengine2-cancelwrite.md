---
UID: NF:imapi2.IWriteEngine2.CancelWrite
title: IWriteEngine2::CancelWrite (imapi2.h)
description: Cancels a write operation that is in progress.
helpviewer_keywords: ["CancelWrite","CancelWrite method [IMAPI]","CancelWrite method [IMAPI]","IWriteEngine2 interface","IWriteEngine2 interface [IMAPI]","CancelWrite method","IWriteEngine2.CancelWrite","IWriteEngine2::CancelWrite","imapi.iwriteengine2_cancelwrite","imapi2/IWriteEngine2::CancelWrite"]
old-location: imapi\iwriteengine2_cancelwrite.htm
tech.root: imapi
ms.assetid: cd658bd3-71ab-4e63-adec-8b7405a76c12
ms.date: 12/05/2018
ms.keywords: CancelWrite, CancelWrite method [IMAPI], CancelWrite method [IMAPI],IWriteEngine2 interface, IWriteEngine2 interface [IMAPI],CancelWrite method, IWriteEngine2.CancelWrite, IWriteEngine2::CancelWrite, imapi.iwriteengine2_cancelwrite, imapi2/IWriteEngine2::CancelWrite
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
 - IWriteEngine2::CancelWrite
 - imapi2/IWriteEngine2::CancelWrite
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
 - IWriteEngine2.CancelWrite
---

# IWriteEngine2::CancelWrite


## -description

Cancels a write operation that is in progress.



## -returns

The following values are returned on success, but other success codes may be returned as a result of implementation: The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

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
<dt><b>S_IMAPI_WRITE_NOT_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
The 'write' operation initiated by the last call to <a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-writesection">IWriteEngine2::WriteSection</a> has not yet begun, and cannot be canceled.   It is recommended to call  <a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-cancelwrite">IWriteEngine2::CancelWrite</a>  until a different success code is returned.

Value: 0x00AA0302L

</td>
</tr>
</table>
 

The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unspecified failure.

Value: 0x80004005

</td>
</tr>
</table>

## -remarks

To cancel the write operation, you must call this method from the <a href="/windows/desktop/api/imapi2/nf-imapi2-dwriteengine2events-update">DWriteEngine2Events::Update</a> event handler that you implemented.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-dwriteengine2events">DWriteEngine2Events</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2">IWriteEngine2</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-writesection">IWriteEngine2::WriteSection</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-get_writeinprogress">IWriteEngine2::get_WriteInProgress</a>
