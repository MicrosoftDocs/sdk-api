---
UID: NF:imapi2.IMultisessionSequential.get_LastWrittenAddressOfPreviousSession
title: IMultisessionSequential::get_LastWrittenAddressOfPreviousSession (imapi2.h)
description: Retrieves the last sector written in the previous session on the media.
helpviewer_keywords: ["IMultisessionSequential interface [IMAPI]","get_LastWrittenAddressOfPreviousSession method","IMultisessionSequential.get_LastWrittenAddressOfPreviousSession","IMultisessionSequential::get_LastWrittenAddressOfPreviousSession","get_LastWrittenAddressOfPreviousSession","get_LastWrittenAddressOfPreviousSession method [IMAPI]","get_LastWrittenAddressOfPreviousSession method [IMAPI]","IMultisessionSequential interface","imapi.imultisessionsequential_get_lastwrittenaddressofprevioussession","imapi2/IMultisessionSequential::get_LastWrittenAddressOfPreviousSession"]
old-location: imapi\imultisessionsequential_get_lastwrittenaddressofprevioussession.htm
tech.root: imapi
ms.assetid: a37aa4d1-0862-463d-acf1-3a85e491ef26
ms.date: 12/05/2018
ms.keywords: IMultisessionSequential interface [IMAPI],get_LastWrittenAddressOfPreviousSession method, IMultisessionSequential.get_LastWrittenAddressOfPreviousSession, IMultisessionSequential::get_LastWrittenAddressOfPreviousSession, get_LastWrittenAddressOfPreviousSession, get_LastWrittenAddressOfPreviousSession method [IMAPI], get_LastWrittenAddressOfPreviousSession method [IMAPI],IMultisessionSequential interface, imapi.imultisessionsequential_get_lastwrittenaddressofprevioussession, imapi2/IMultisessionSequential::get_LastWrittenAddressOfPreviousSession
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
 - IMultisessionSequential::get_LastWrittenAddressOfPreviousSession
 - imapi2/IMultisessionSequential::get_LastWrittenAddressOfPreviousSession
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
 - IMultisessionSequential.get_LastWrittenAddressOfPreviousSession
---

# IMultisessionSequential::get_LastWrittenAddressOfPreviousSession


## -description

Retrieves the last sector written in the previous session on the media.

## -parameters

### -param value

Sector number that identifies the last sector written in the previous write session.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

Value: 0x80004001

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential">IMultisessionSequential</a>