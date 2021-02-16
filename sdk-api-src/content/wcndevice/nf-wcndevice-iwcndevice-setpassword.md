---
UID: NF:wcndevice.IWCNDevice.SetPassword
title: IWCNDevice::SetPassword (wcndevice.h)
description: The IWCNDevice::SetPassword method configures the authentication method value, and if required, a password used for the pending session. This method may only be called prior to IWCNDevice::Connect.
helpviewer_keywords: ["IWCNDevice interface [Windows Connect Now]","SetPassword method","IWCNDevice.SetPassword","IWCNDevice::SetPassword","SetPassword","SetPassword method [Windows Connect Now]","SetPassword method [Windows Connect Now]","IWCNDevice interface","WCN_PASSWORD_TYPE_PIN","WCN_PASSWORD_TYPE_PUSH_BUTTON","wcn.iwcndevice_setpassword","wcndevice/IWCNDevice::SetPassword"]
old-location: wcn\iwcndevice_setpassword.htm
tech.root: wcn
ms.assetid: 51d03336-3861-4585-b493-d6765c28b1eb
ms.date: 12/05/2018
ms.keywords: IWCNDevice interface [Windows Connect Now],SetPassword method, IWCNDevice.SetPassword, IWCNDevice::SetPassword, SetPassword, SetPassword method [Windows Connect Now], SetPassword method [Windows Connect Now],IWCNDevice interface, WCN_PASSWORD_TYPE_PIN, WCN_PASSWORD_TYPE_PUSH_BUTTON, wcn.iwcndevice_setpassword, wcndevice/IWCNDevice::SetPassword
req.header: wcndevice.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcnDevice.idl
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
 - IWCNDevice::SetPassword
 - wcndevice/IWCNDevice::SetPassword
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WcnDevice.h
api_name:
 - IWCNDevice.SetPassword
---

# IWCNDevice::SetPassword


## -description

The <b>IWCNDevice::SetPassword</b> method configures the authentication method value, and if required, a password used for the pending session.  This method may  only be called prior to <a href="/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-connect">IWCNDevice::Connect</a>.

## -parameters

### -param Type [in]

A <b>WCN_PASSWORD_TYPE</b> value that specifies the authentication method used for the session.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WCN_PASSWORD_TYPE_PUSH_BUTTON"></a><a id="wcn_password_type_push_button"></a><dl>
<dt><b>WCN_PASSWORD_TYPE_PUSH_BUTTON</b></dt>
</dl>
</td>
<td width="60%">
Use PushButton authentication.  The value of <i>dwPasswordLength</i> must be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="WCN_PASSWORD_TYPE_PIN"></a><a id="wcn_password_type_pin"></a><dl>
<dt><b>WCN_PASSWORD_TYPE_PIN</b></dt>
</dl>
</td>
<td width="60%">
Use PIN-based authentication.

</td>
</tr>
</table>

### -param dwPasswordLength [in]

Number of bytes in the buffer <i>pbPassword</i>.

### -param pbPassword [in]

A byte array of the password, encoded in ASCII.

## -returns

This method can return one of these values.

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
The password will be used for the pending session.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The password type is WCN_PASSWORD_TYPE_PUSH_BUTTON and the password length is not zero.

The password type is not WCN_PASSWORD_TYPE_PUSH_BUTTON or WCN_PASSWORD_TYPE_PIN.

</td>
</tr>
</table>

## -remarks

The byte array is not <b>NULL</b>-terminated.  For example, if the password is a 4-digit PIN, you should pass dwPasswordLength as 4 and pbPassword should point to a 4-byte array containing the PIN in ASCII.

## -see-also

<a href="/windows/desktop/api/wcndevice/nn-wcndevice-iwcndevice">IWCNDevice</a>



<a href="/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-connect">IWCNDevice::Connect</a>



<b>WCN_PASSWORD_TYPE</b>