---
UID: NF:rrascfg.IEAPProviderConfig.ServerInvokeConfigUI
title: IEAPProviderConfig::ServerInvokeConfigUI (rrascfg.h)
description: The system calls the ServerInvokeConfigUI method to invoke the configuration user interface for EAP authentication between a remote access client and server.
helpviewer_keywords: ["IEAPProviderConfig interface [EAP]","ServerInvokeConfigUI method","IEAPProviderConfig.ServerInvokeConfigUI","IEAPProviderConfig::ServerInvokeConfigUI","ServerInvokeConfigUI","ServerInvokeConfigUI method [EAP]","ServerInvokeConfigUI method [EAP]","IEAPProviderConfig interface","_eap_ieapproviderconfig_serverinvokeconfigui","eap.ieapproviderconfig_serverinvokeconfigui","rrascfg/IEAPProviderConfig::ServerInvokeConfigUI"]
old-location: eap\ieapproviderconfig_serverinvokeconfigui.htm
tech.root: EAP
ms.assetid: 95d98664-e108-41d5-8ed0-49867563df43
ms.date: 12/05/2018
ms.keywords: IEAPProviderConfig interface [EAP],ServerInvokeConfigUI method, IEAPProviderConfig.ServerInvokeConfigUI, IEAPProviderConfig::ServerInvokeConfigUI, ServerInvokeConfigUI, ServerInvokeConfigUI method [EAP], ServerInvokeConfigUI method [EAP],IEAPProviderConfig interface, _eap_ieapproviderconfig_serverinvokeconfigui, eap.ieapproviderconfig_serverinvokeconfigui, rrascfg/IEAPProviderConfig::ServerInvokeConfigUI
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
 - IEAPProviderConfig::ServerInvokeConfigUI
 - rrascfg/IEAPProviderConfig::ServerInvokeConfigUI
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
 - IEAPProviderConfig.ServerInvokeConfigUI
---

# IEAPProviderConfig::ServerInvokeConfigUI


## -description

The system calls the <b>ServerInvokeConfigUI</b> method to invoke the configuration user interface for EAP authentication between a remote access client and server.

## -parameters

### -param dwEapTypeId

Specifies the EAP for which to invoke the configuration user interface.

### -param uConnectionParam

Specifies the configuration session for which to invoke the user interface.

### -param hWnd

Handle to the parent window for the configuration user interface.

### -param uReserved1

This parameter is reserved and should be zero.

### -param uReserved2

This parameter is reserved and should be zero.

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

The DLL that implements 
<a href="/previous-versions/windows/desktop/api/rrascfg/nn-rrascfg-ieapproviderconfig">IEAPProviderConfig</a> may support more than one authentication protocol. The <i>dwEapTypeId</i> parameter specifies for which authentication protocol to invoke the configuration user interface.

## -see-also

[EAP Interfaces](/windows/win32/eap/eap-interfaces)



[Extensible Authentication Protocol Reference](/windows/win32/eap/extensible-authentication-protocol-reference)



<a href="/previous-versions/windows/desktop/api/rrascfg/nn-rrascfg-ieapproviderconfig">IEAPProviderConfig</a>



<a href="/previous-versions/windows/desktop/api/rrascfg/nf-rrascfg-ieapproviderconfig-initialize">IEAPProviderConfig::Initialize</a>



<a href="/previous-versions/windows/desktop/api/rrascfg/nf-rrascfg-ieapproviderconfig-routerinvokeconfigui">IEAPProviderConfig::RouterInvokeConfigUI</a>



<a href="/previous-versions/windows/desktop/api/rrascfg/nf-rrascfg-ieapproviderconfig-routerinvokecredentialsui">IEAPProviderConfig::RouterInvokeCredentialsUI</a>



<a href="/previous-versions/windows/desktop/api/rrascfg/nf-rrascfg-ieapproviderconfig-uninitialize">IEAPProviderConfig::Uninitialize</a>