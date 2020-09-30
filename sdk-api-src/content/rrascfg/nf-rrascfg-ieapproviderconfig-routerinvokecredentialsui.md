---
UID: NF:rrascfg.IEAPProviderConfig.RouterInvokeCredentialsUI
title: IEAPProviderConfig::RouterInvokeCredentialsUI (rrascfg.h)
description: The system calls the RouterInvokeCredentialsUI method to invoke the credentials user interface for EAP authentication between two routers.
helpviewer_keywords: ["IEAPProviderConfig interface [EAP]","RouterInvokeCredentialsUI method","IEAPProviderConfig.RouterInvokeCredentialsUI","IEAPProviderConfig::RouterInvokeCredentialsUI","RouterInvokeCredentialsUI","RouterInvokeCredentialsUI method [EAP]","RouterInvokeCredentialsUI method [EAP]","IEAPProviderConfig interface","_eap_ieapproviderconfig_routerinvokecredentialsui","eap.ieapproviderconfig_routerinvokecredentialsui","rrascfg/IEAPProviderConfig::RouterInvokeCredentialsUI"]
old-location: eap\ieapproviderconfig_routerinvokecredentialsui.htm
tech.root: EAP
ms.assetid: 23b64f95-1f21-4e81-a094-081a95057aef
ms.date: 12/05/2018
ms.keywords: IEAPProviderConfig interface [EAP],RouterInvokeCredentialsUI method, IEAPProviderConfig.RouterInvokeCredentialsUI, IEAPProviderConfig::RouterInvokeCredentialsUI, RouterInvokeCredentialsUI, RouterInvokeCredentialsUI method [EAP], RouterInvokeCredentialsUI method [EAP],IEAPProviderConfig interface, _eap_ieapproviderconfig_routerinvokecredentialsui, eap.ieapproviderconfig_routerinvokecredentialsui, rrascfg/IEAPProviderConfig::RouterInvokeCredentialsUI
req.header: rrascfg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IEAPProviderConfig::RouterInvokeCredentialsUI
 - rrascfg/IEAPProviderConfig::RouterInvokeCredentialsUI
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Rrascfg.h
api_name:
 - IEAPProviderConfig.RouterInvokeCredentialsUI
---

# IEAPProviderConfig::RouterInvokeCredentialsUI


## -description

The system calls the <b>RouterInvokeCredentialsUI</b> method to invoke the credentials user interface for EAP authentication between two routers.

## -parameters

### -param dwEapTypeId

Specifies the EAP for which to invoke the configuration user interface.

### -param uConnectionParam

Specifies the configuration session for which to invoke the user interface.

### -param hwndParent

Handle to the parent window for the configuration user interface.

### -param dwFlags

Specifies the RAS_EAP_FLAG_ROUTER flag. This is the only valid flag for this parameter. It indicates that authentication is between two routers. This parameter always includes this flag.

### -param pConnectionDataIn

Pointer to the current configuration data for the interface.

### -param dwSizeOfConnectionDataIn

Specifies the size of the current configuration data pointed to by the <i>pConnectionDataIn</i> parameter.

### -param pUserDataIn

Pointer to the current credential data for the interface.

### -param dwSizeOfUserDataIn

Specifies the size of the current credentials data.

### -param ppUserDataOut

Pointer to a pointer to a buffer to receive the new credentials data for the interface.

### -param pdwSizeOfUserDataOut

Pointer to a <b>DWORD</b> variable to receive the size of the new credentials data.

## -returns

If the function succeeds, the return value should be <b>S_OK</b>.

If the function fails, the return value should be one of the following codes.

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
Non-specific error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method failed because it was unable to allocate the required memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error occurred.

</td>
</tr>
</table>

## -see-also

[EAP Interfaces](/windows/win32/eap/eap-interfaces)



[Extensible Authentication Protocol Reference](/windows/win32/eap/extensible-authentication-protocol-reference)



<a href="/previous-versions/windows/desktop/api/rrascfg/nn-rrascfg-ieapproviderconfig">IEAPProviderConfig</a>



<a href="/previous-versions/windows/desktop/api/rrascfg/nf-rrascfg-ieapproviderconfig-initialize">IEAPProviderConfig::Initialize</a>



<a href="/previous-versions/windows/desktop/api/rrascfg/nf-rrascfg-ieapproviderconfig-routerinvokeconfigui">IEAPProviderConfig::RouterInvokeConfigUI</a>



<a href="/previous-versions/windows/desktop/api/rrascfg/nf-rrascfg-ieapproviderconfig-serverinvokeconfigui">IEAPProviderConfig::ServerInvokeConfigUI</a>



<a href="/previous-versions/windows/desktop/api/rrascfg/nf-rrascfg-ieapproviderconfig-uninitialize">IEAPProviderConfig::Uninitialize</a>