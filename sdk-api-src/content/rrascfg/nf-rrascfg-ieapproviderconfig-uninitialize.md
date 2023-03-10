---
UID: NF:rrascfg.IEAPProviderConfig.Uninitialize
title: IEAPProviderConfig::Uninitialize (rrascfg.h)
description: The system calls the Uninitialize method to shut down the specified EAP configuration session.
helpviewer_keywords: ["IEAPProviderConfig interface [EAP]","Uninitialize method","IEAPProviderConfig.Uninitialize","IEAPProviderConfig::Uninitialize","Uninitialize","Uninitialize method [EAP]","Uninitialize method [EAP]","IEAPProviderConfig interface","_eap_ieapproviderconfig_uninitialize","eap.ieapproviderconfig_uninitialize","rrascfg/IEAPProviderConfig::Uninitialize"]
old-location: eap\ieapproviderconfig_uninitialize.htm
tech.root: EAP
ms.assetid: f96ffa3f-cd3c-4979-87b3-1a2afb7a3621
ms.date: 12/05/2018
ms.keywords: IEAPProviderConfig interface [EAP],Uninitialize method, IEAPProviderConfig.Uninitialize, IEAPProviderConfig::Uninitialize, Uninitialize, Uninitialize method [EAP], Uninitialize method [EAP],IEAPProviderConfig interface, _eap_ieapproviderconfig_uninitialize, eap.ieapproviderconfig_uninitialize, rrascfg/IEAPProviderConfig::Uninitialize
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
 - IEAPProviderConfig::Uninitialize
 - rrascfg/IEAPProviderConfig::Uninitialize
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
 - IEAPProviderConfig.Uninitialize
---

# IEAPProviderConfig::Uninitialize


## -description

The system calls the <b>Uninitialize</b> method to shut down the specified EAP configuration session.

## -parameters

### -param dwEapTypeId

Specifies the EAP for which to shut down the configuration session.

### -param uConnectionParam

Specifies the configuration session to shut down.

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
The method failed because it was unable to allocate required memory.

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

## -remarks

The configuration UI should allow the user to configure the EAP provider on a remote computer. Delete the connection to the remote computer during the call to <b>Uninitialize</b>.

The DLL that implements 
<a href="/previous-versions/windows/desktop/api/rrascfg/nn-rrascfg-ieapproviderconfig">IEAPProviderConfig</a> may support more than one authentication protocol. The <i>dwEapTypeId</i> parameter specifies the authentication protocol to shut down the configuration session for.

## -see-also

[EAP Interfaces](/windows/win32/eap/eap-interfaces)



[Extensible Authentication Protocol Reference](/windows/win32/eap/extensible-authentication-protocol-reference)



<a href="/previous-versions/windows/desktop/api/rrascfg/nn-rrascfg-ieapproviderconfig">IEAPProviderConfig</a>



<a href="/previous-versions/windows/desktop/api/rrascfg/nf-rrascfg-ieapproviderconfig-initialize">IEAPProviderConfig::Initialize</a>



<a href="/previous-versions/windows/desktop/api/rrascfg/nf-rrascfg-ieapproviderconfig-routerinvokeconfigui">IEAPProviderConfig::RouterInvokeConfigUI</a>



<a href="/previous-versions/windows/desktop/api/rrascfg/nf-rrascfg-ieapproviderconfig-routerinvokecredentialsui">IEAPProviderConfig::RouterInvokeCredentialsUI</a>



<a href="/previous-versions/windows/desktop/api/rrascfg/nf-rrascfg-ieapproviderconfig-serverinvokeconfigui">IEAPProviderConfig::ServerInvokeConfigUI</a>