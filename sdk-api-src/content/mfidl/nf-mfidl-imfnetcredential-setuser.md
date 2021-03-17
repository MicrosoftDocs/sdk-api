---
UID: NF:mfidl.IMFNetCredential.SetUser
title: IMFNetCredential::SetUser (mfidl.h)
description: Sets the user name.
helpviewer_keywords: ["026a822a-4e48-4fc8-9781-5e427528a4d2","IMFNetCredential interface [Media Foundation]","SetUser method","IMFNetCredential.SetUser","IMFNetCredential::SetUser","SetUser","SetUser method [Media Foundation]","SetUser method [Media Foundation]","IMFNetCredential interface","mf.imfnetcredential_setuser","mfidl/IMFNetCredential::SetUser"]
old-location: mf\imfnetcredential_setuser.htm
tech.root: mf
ms.assetid: 026a822a-4e48-4fc8-9781-5e427528a4d2
ms.date: 12/05/2018
ms.keywords: 026a822a-4e48-4fc8-9781-5e427528a4d2, IMFNetCredential interface [Media Foundation],SetUser method, IMFNetCredential.SetUser, IMFNetCredential::SetUser, SetUser, SetUser method [Media Foundation], SetUser method [Media Foundation],IMFNetCredential interface, mf.imfnetcredential_setuser, mfidl/IMFNetCredential::SetUser
req.header: mfidl.h
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFNetCredential::SetUser
 - mfidl/IMFNetCredential::SetUser
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFNetCredential.SetUser
---

# IMFNetCredential::SetUser


## -description

Sets the user name.

## -parameters

### -param pbData [in]

Pointer to a buffer that contains the user name. If <i>fDataIsEncrypted</i> is <b>FALSE</b>, the buffer is a wide-character string. Otherwise, the buffer contains encrypted data.

### -param cbData [in]

Size of <i>pbData</i>, in bytes. If <i>fDataIsEncrypted</i> is <b>FALSE</b>, the size includes the terminating null character.

### -param fDataIsEncrypted [in]

If <b>TRUE</b>, the user name is encrypted. Otherwise, the user name is not encrypted.

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

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential">IMFNetCredential</a>