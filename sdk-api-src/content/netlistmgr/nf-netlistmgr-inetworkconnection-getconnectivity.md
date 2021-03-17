---
UID: NF:netlistmgr.INetworkConnection.GetConnectivity
title: INetworkConnection::GetConnectivity (netlistmgr.h)
description: The GetConnectivity method returns the connectivity state of the network connection.
helpviewer_keywords: ["GetConnectivity","GetConnectivity method [Network Awareness]","GetConnectivity method [Network Awareness]","INetworkConnection interface","INetworkConnection interface [Network Awareness]","GetConnectivity method","INetworkConnection.GetConnectivity","INetworkConnection::GetConnectivity","netlistmgr/INetworkConnection::GetConnectivity","nla.inetworkconnection_getconnectivity"]
old-location: nla\inetworkconnection_getconnectivity.htm
tech.root: nla
ms.assetid: 63fe54f7-c5e5-4dac-ad06-5ebfdb3a3419
ms.date: 12/05/2018
ms.keywords: GetConnectivity, GetConnectivity method [Network Awareness], GetConnectivity method [Network Awareness],INetworkConnection interface, INetworkConnection interface [Network Awareness],GetConnectivity method, INetworkConnection.GetConnectivity, INetworkConnection::GetConnectivity, netlistmgr/INetworkConnection::GetConnectivity, nla.inetworkconnection_getconnectivity
req.header: netlistmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Netlistmgr.idl
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
 - INetworkConnection::GetConnectivity
 - netlistmgr/INetworkConnection::GetConnectivity
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Netlistmgr.h
api_name:
 - INetworkConnection.GetConnectivity
---

# INetworkConnection::GetConnectivity


## -description

The <b>GetConnectivity</b> method returns the connectivity state of the network connection.

## -parameters

### -param pConnectivity [out]

Pointer to a <a href="/windows/desktop/api/netlistmgr/ne-netlistmgr-nlm_connectivity">NLM_CONNECTIVITY</a> enumeration value that contains  a bitmask that specifies the connectivity of this network connection.

## -returns

Returns S_OK if the method succeeds.

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworkconnection">INetworkConnection</a>