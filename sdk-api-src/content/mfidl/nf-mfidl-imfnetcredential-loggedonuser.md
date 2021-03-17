---
UID: NF:mfidl.IMFNetCredential.LoggedOnUser
title: IMFNetCredential::LoggedOnUser (mfidl.h)
description: Queries whether logged-on credentials should be used.
helpviewer_keywords: ["70f3dc70-ed6b-417c-93cb-e00efcdb43ec","IMFNetCredential interface [Media Foundation]","LoggedOnUser method","IMFNetCredential.LoggedOnUser","IMFNetCredential::LoggedOnUser","LoggedOnUser","LoggedOnUser method [Media Foundation]","LoggedOnUser method [Media Foundation]","IMFNetCredential interface","mf.imfnetcredential_loggedonuser","mfidl/IMFNetCredential::LoggedOnUser"]
old-location: mf\imfnetcredential_loggedonuser.htm
tech.root: mf
ms.assetid: 70f3dc70-ed6b-417c-93cb-e00efcdb43ec
ms.date: 12/05/2018
ms.keywords: 70f3dc70-ed6b-417c-93cb-e00efcdb43ec, IMFNetCredential interface [Media Foundation],LoggedOnUser method, IMFNetCredential.LoggedOnUser, IMFNetCredential::LoggedOnUser, LoggedOnUser, LoggedOnUser method [Media Foundation], LoggedOnUser method [Media Foundation],IMFNetCredential interface, mf.imfnetcredential_loggedonuser, mfidl/IMFNetCredential::LoggedOnUser
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
 - IMFNetCredential::LoggedOnUser
 - mfidl/IMFNetCredential::LoggedOnUser
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
 - IMFNetCredential.LoggedOnUser
---

# IMFNetCredential::LoggedOnUser


## -description

Queries whether logged-on credentials should be used.

## -parameters

### -param pfLoggedOnUser [in]

Receives a Boolean value. If logged-on credentials should be used, the value is <b>TRUE</b>. Otherwise, the value is <b>FALSE</b>.

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