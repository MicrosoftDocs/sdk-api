---
UID: NF:rrascfg.IEAPProviderConfig.Initialize
title: IEAPProviderConfig::Initialize (rrascfg.h)
description: The system calls the Initialize method to initialize an EAP configuration session with the specified computer.
helpviewer_keywords: ["IEAPProviderConfig interface [EAP]","Initialize method","IEAPProviderConfig.Initialize","IEAPProviderConfig::Initialize","Initialize","Initialize method [EAP]","Initialize method [EAP]","IEAPProviderConfig interface","_eap_ieapproviderconfig_initialize","eap.ieapproviderconfig_initialize","rrascfg/IEAPProviderConfig::Initialize"]
old-location: eap\ieapproviderconfig_initialize.htm
tech.root: EAP
ms.assetid: 6d347387-7f8f-478b-a115-f6960e6f856e
ms.date: 12/05/2018
ms.keywords: IEAPProviderConfig interface [EAP],Initialize method, IEAPProviderConfig.Initialize, IEAPProviderConfig::Initialize, Initialize, Initialize method [EAP], Initialize method [EAP],IEAPProviderConfig interface, _eap_ieapproviderconfig_initialize, eap.ieapproviderconfig_initialize, rrascfg/IEAPProviderConfig::Initialize
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
 - IEAPProviderConfig::Initialize
 - rrascfg/IEAPProviderConfig::Initialize
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
 - IEAPProviderConfig.Initialize
---

# IEAPProviderConfig::Initialize


## -description

The system calls the <b>Initialize</b> method to initialize an EAP configuration session with the specified computer.

## -parameters

### -param pszMachineName

Pointer to a null-terminated string that contains the name of the computer on which to configure EAP. String length is not limited.

### -param dwEapTypeId

Specifies the EAP for which to initialize a configuration session.

### -param puConnectionParam

Pointer to an unsigned integer variable. On successful return, the value of this variable identifies this configuration session.

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

The configuration UI should allow the user to configure the EAP provider on a remote computer. Establish the connection to the remote computer during the call to <b>Initialize</b>.

The DLL that implements 
<a href="/previous-versions/windows/desktop/api/rrascfg/nn-rrascfg-ieapproviderconfig">IEAPProviderConfig</a> can support more than one authentication protocol. The <i>dwEapTypeId</i> parameter specifies the  authentication protocol to initialize a configuration session for.

## -see-also

[EAP Interfaces](/windows/win32/eap/eap-interfaces)



[Extensible Authentication Protocol Reference](/windows/win32/eap/extensible-authentication-protocol-reference)



<a href="/previous-versions/windows/desktop/api/rrascfg/nn-rrascfg-ieapproviderconfig">IEAPProviderConfig</a>



<a href="/previous-versions/windows/desktop/api/rrascfg/nf-rrascfg-ieapproviderconfig-routerinvokeconfigui">IEAPProviderConfig::RouterInvokeConfigUI</a>



<a href="/previous-versions/windows/desktop/api/rrascfg/nf-rrascfg-ieapproviderconfig-routerinvokecredentialsui">IEAPProviderConfig::RouterInvokeCredentialsUI</a>



<a href="/previous-versions/windows/desktop/api/rrascfg/nf-rrascfg-ieapproviderconfig-serverinvokeconfigui">IEAPProviderConfig::ServerInvokeConfigUI</a>



<a href="/previous-versions/windows/desktop/api/rrascfg/nf-rrascfg-ieapproviderconfig-uninitialize">IEAPProviderConfig::Uninitialize</a>