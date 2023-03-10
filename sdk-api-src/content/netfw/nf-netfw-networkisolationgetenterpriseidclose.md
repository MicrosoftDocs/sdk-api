---
UID: NF:netfw.NetworkIsolationGetEnterpriseIdClose
title: NetworkIsolationGetEnterpriseIdClose function (netfw.h)
description: This API is used for closing the handle returned by NetworkIsolationGetEnterpriseIdAsync as well as for synchronizing the operation.
helpviewer_keywords: ["NetworkIsolationGetEnterpriseIdClose","NetworkIsolationGetEnterpriseIdClose function [ICS/ICF]","ics.networkisolationgetenterpriseidclose","netfw/NetworkIsolationGetEnterpriseIdClose"]
old-location: ics\networkisolationgetenterpriseidclose.htm
tech.root: ics
ms.assetid: 85FE7431-CC20-4CD2-9853-9B81BB8B7160
ms.date: 12/05/2018
ms.keywords: NetworkIsolationGetEnterpriseIdClose, NetworkIsolationGetEnterpriseIdClose function [ICS/ICF], ics.networkisolationgetenterpriseidclose, netfw/NetworkIsolationGetEnterpriseIdClose
req.header: netfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetworkIsolationGetEnterpriseIdClose
 - netfw/NetworkIsolationGetEnterpriseIdClose
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - firewallapi.dll
api_name:
 - NetworkIsolationGetEnterpriseIdClose
---

# NetworkIsolationGetEnterpriseIdClose function


## -description

This API is used for closing the handle returned by  <a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationgetenterpriseidasync">NetworkIsolationGetEnterpriseIdAsync</a> as well as for synchronizing the operation.

Example of NetworkIsolationGetEnterpriseIdClose usage: https://github.com/microsoft/EnterpriseStateClassify

## -parameters

### -param hOperation [in]

The handle to release.

### -param bWaitForOperation [in]

Indicates whether to wait for synchronization.

## -returns

Returns ERROR_SUCCESS if successful, or an error value otherwise.