---
UID: NF:imapi2.IWriteEngine2.get_UseStreamingWrite12
title: IWriteEngine2::get_UseStreamingWrite12 (imapi2.h)
description: Retrieves a value that indicates if the write operations use the WRITE12 or WRITE10 command.
helpviewer_keywords: ["IWriteEngine2 interface [IMAPI]","get_UseStreamingWrite12 method","IWriteEngine2.get_UseStreamingWrite12","IWriteEngine2::get_UseStreamingWrite12","get_UseStreamingWrite12","get_UseStreamingWrite12 method [IMAPI]","get_UseStreamingWrite12 method [IMAPI]","IWriteEngine2 interface","imapi.iwriteengine2_get_usestreamingwrite12","imapi2/IWriteEngine2::get_UseStreamingWrite12"]
old-location: imapi\iwriteengine2_get_usestreamingwrite12.htm
tech.root: imapi
ms.assetid: 28f5673e-73f4-4bec-bdee-49cbd030a0d6
ms.date: 12/05/2018
ms.keywords: IWriteEngine2 interface [IMAPI],get_UseStreamingWrite12 method, IWriteEngine2.get_UseStreamingWrite12, IWriteEngine2::get_UseStreamingWrite12, get_UseStreamingWrite12, get_UseStreamingWrite12 method [IMAPI], get_UseStreamingWrite12 method [IMAPI],IWriteEngine2 interface, imapi.iwriteengine2_get_usestreamingwrite12, imapi2/IWriteEngine2::get_UseStreamingWrite12
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
 - IWriteEngine2::get_UseStreamingWrite12
 - imapi2/IWriteEngine2::get_UseStreamingWrite12
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
 - IWriteEngine2.get_UseStreamingWrite12
---

# IWriteEngine2::get_UseStreamingWrite12


## -description

Retrieves a value that indicates if the write operations use the WRITE12 or WRITE10 command.

## -parameters

### -param value [out]

If VARIANT_TRUE, the write operations use the WRITE12 command with the streaming bit set to one. Otherwise, if VARIANT_FALSE, the write operations use the WRITE10 command.

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



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-writesection">IWriteEngine2::WriteSection</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-put_usestreamingwrite12">IWriteEngine2::put_UseStreamingWrite12</a>