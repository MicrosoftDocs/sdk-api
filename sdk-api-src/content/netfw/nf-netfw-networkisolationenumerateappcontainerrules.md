---
UID: NF:netfw.NetworkIsolationEnumerateAppContainerRules
title: NetworkIsolationEnumerateAppContainerRules function (netfw.h)
description: Enumerates all of the rules related to app containers.
helpviewer_keywords: ["NetworkIsolationEnumerateAppContainerRules","NetworkIsolationEnumerateAppContainerRules function [ICS/ICF]","ics.networkisolationenumerateappcontainerrules","netfw/NetworkIsolationEnumerateAppContainerRules"]
old-location: ics\networkisolationenumerateappcontainerrules.htm
tech.root: ics
ms.assetid: 53c9cd2c-06da-41ba-bbd8-bd695fb7fabf
ms.date: 12/05/2018
ms.keywords: NetworkIsolationEnumerateAppContainerRules, NetworkIsolationEnumerateAppContainerRules function [ICS/ICF], ics.networkisolationenumerateappcontainerrules, netfw/NetworkIsolationEnumerateAppContainerRules
f1_keywords:
- netfw/NetworkIsolationEnumerateAppContainerRules
dev_langs:
- c++
req.header: netfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: Firewallapi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- firewallapi.dll
- API-MS-Win-Net-Isolation-l1-1-0.dll
- API-MS-Win-Net-Isolation-l1-1-1.dll
- wfapihost.dll
api_name:
- NetworkIsolationEnumerateAppContainerRules
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NetworkIsolationEnumerateAppContainerRules function


## -description


The <b>NetworkIsolationEnumerateAppContainerRules</b> function enumerates all of the rules related to app containers.


## -parameters




### -param newEnum [out]

Type: <b>IEnumVARIANT**</b>

Enumerator interface of an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrule3">INetFwRule3</a> object that represents the rules enforcing app containers.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



