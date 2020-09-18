---
UID: NF:mfidl.IMFProtectedEnvironmentAccess.Call
title: IMFProtectedEnvironmentAccess::Call (mfidl.h)
description: Allows content protection systems to access the protected environment.
helpviewer_keywords: ["Call","Call method [Media Foundation]","Call method [Media Foundation]","IMFProtectedEnvironmentAccess interface","IMFProtectedEnvironmentAccess interface [Media Foundation]","Call method","IMFProtectedEnvironmentAccess.Call","IMFProtectedEnvironmentAccess::Call","mf.imfprotectedenvironmentaccess_call","mfidl/IMFProtectedEnvironmentAccess::Call"]
old-location: mf\imfprotectedenvironmentaccess_call.htm
tech.root: mf
ms.assetid: 805473c4-a2c9-483a-9a2c-29a9c63dd58c
ms.date: 12/05/2018
ms.keywords: Call, Call method [Media Foundation], Call method [Media Foundation],IMFProtectedEnvironmentAccess interface, IMFProtectedEnvironmentAccess interface [Media Foundation],Call method, IMFProtectedEnvironmentAccess.Call, IMFProtectedEnvironmentAccess::Call, mf.imfprotectedenvironmentaccess_call, mfidl/IMFProtectedEnvironmentAccess::Call
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IMFProtectedEnvironmentAccess::Call
 - mfidl/IMFProtectedEnvironmentAccess::Call
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mfidl.h
api_name:
 - IMFProtectedEnvironmentAccess.Call
---

# IMFProtectedEnvironmentAccess::Call


## -description

Allows content protection systems to access the protected environment.

## -parameters

### -param inputLength

The length in bytes of the input data.

### -param input

A pointer to the input data.

### -param outputLength

The length in bytes of the output data.

### -param output

A pointer to the output data.

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

## -remarks

See  <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreateprotectedenvironmentaccess">MFCreateProtectedEnvironmentAccess</a> for an example of how to create an <a href="/windows/desktop/api/mfidl/nn-mfidl-imfprotectedenvironmentaccess">IMFProtectedEnvironmentAccess</a> object and use the <b>Call</b> method.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfprotectedenvironmentaccess">IMFProtectedEnvironmentAccess</a>



<a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreateprotectedenvironmentaccess">MFCreateProtectedEnvironmentAccess</a>