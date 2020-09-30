---
UID: NN:rrascfg.IEAPProviderConfig
title: IEAPProviderConfig (rrascfg.h)
description: UI for EAP provider.
helpviewer_keywords: ["IEAPProviderConfig","IEAPProviderConfig interface [EAP]","IEAPProviderConfig interface [EAP]","described","_eap_ieapproviderconfig","eap.ieapproviderconfig","rrascfg/IEAPProviderConfig"]
old-location: eap\ieapproviderconfig.htm
tech.root: EAP
ms.assetid: 1e0283b7-ceb3-4c8a-99d9-1a1f1eb5eeb0
ms.date: 12/05/2018
ms.keywords: IEAPProviderConfig, IEAPProviderConfig interface [EAP], IEAPProviderConfig interface [EAP],described, _eap_ieapproviderconfig, eap.ieapproviderconfig, rrascfg/IEAPProviderConfig
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
 - IEAPProviderConfig
 - rrascfg/IEAPProviderConfig
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rrascfg.h
api_name:
 - IEAPProviderConfig
---

# IEAPProviderConfig interface


## -description

The **IEAPProviderConfig** interface is used to initialize, configure and shut down EAP configuration sessions.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEAPProviderConfig</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEAPProviderConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEAPProviderConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/rrascfg/nf-rrascfg-ieapproviderconfig-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an EAP configuration session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/rrascfg/nf-rrascfg-ieapproviderconfig-routerinvokeconfigui">RouterInvokeConfigUI</a>
</td>
<td align="left" width="63%">
Invokes the EAP configuration user interface for router-to-router EAP.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/rrascfg/nf-rrascfg-ieapproviderconfig-routerinvokecredentialsui">RouterInvokeCredentialsUI</a>
</td>
<td align="left" width="63%">
Invokes the EAP credentials user interface for router-to-router EAP.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/rrascfg/nf-rrascfg-ieapproviderconfig-serverinvokeconfigui">ServerInvokeConfigUI</a>
</td>
<td align="left" width="63%">
Invokes the EAP configuration user interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/rrascfg/nf-rrascfg-ieapproviderconfig-uninitialize">Uninitialize</a>
</td>
<td align="left" width="63%">
Shuts down an EAP configuration session.

</td>
</tr>
</table>

## -see-also

[EAP Interfaces](/windows/win32/eap/eap-interfaces)



[Extensible Authentication Protocol Reference](/windows/win32/eap/extensible-authentication-protocol-reference)