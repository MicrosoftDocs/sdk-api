---
UID: NF:netfw.NetworkIsolationEnumerateAppContainerRules
title: NetworkIsolationEnumerateAppContainerRules function
author: windows-driver-content
description: Enumerates all of the rules related to app containers.
old-location: ics\networkisolationenumerateappcontainerrules.htm
old-project: ICS
ms.assetid: 53c9cd2c-06da-41ba-bbd8-bd695fb7fabf
ms.author: windowsdriverdev
ms.date: 5/1/2018
ms.keywords: NetworkIsolationEnumerateAppContainerRules, NetworkIsolationEnumerateAppContainerRules function [ICS/ICF], ics.networkisolationenumerateappcontainerrules, netfw/NetworkIsolationEnumerateAppContainerRules
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: NETISO_ERROR_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	firewallapi.dll
-	API-MS-Win-Net-Isolation-l1-1-0.dll
-	API-MS-Win-Net-Isolation-l1-1-1.dll
-	wfapihost.dll
api_name:
-	NetworkIsolationEnumerateAppContainerRules
product: Windows
targetos: Windows
req.lib: 
req.dll: Firewallapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# NetworkIsolationEnumerateAppContainerRules function


## -description


The <b>NetworkIsolationEnumerateAppContainerRules</b> function enumerates all of the rules related to app containers.


## -parameters




### -param newEnum [out]

Type: <b>IEnumVARIANT**</b>

Enumerator interface of an <a href="https://msdn.microsoft.com/72bf5ac3-7ee7-4837-96b2-815b499aac2f">INetFwRule3</a> object that represents the rules enforcing app containers.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



