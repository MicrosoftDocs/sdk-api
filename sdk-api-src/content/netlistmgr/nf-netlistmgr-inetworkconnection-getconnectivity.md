---
UID: NF:netlistmgr.INetworkConnection.GetConnectivity
title: INetworkConnection::GetConnectivity
author: windows-sdk-content
description: The GetConnectivity method returns the connectivity state of the network connection.
old-location: nla\inetworkconnection_getconnectivity.htm
tech.root: nla
ms.assetid: 63fe54f7-c5e5-4dac-ad06-5ebfdb3a3419
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetConnectivity, GetConnectivity method [Network Awareness], GetConnectivity method [Network Awareness],INetworkConnection interface, INetworkConnection interface [Network Awareness],GetConnectivity method, INetworkConnection.GetConnectivity, INetworkConnection::GetConnectivity, netlistmgr/INetworkConnection::GetConnectivity, nla.inetworkconnection_getconnectivity
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Netlistmgr.h
api_name:
 - INetworkConnection.GetConnectivity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetworkConnection::GetConnectivity


## -description


The <b>GetConnectivity</b> method returns the connectivity state of the network connection.


## -parameters




### -param pConnectivity [out]

Pointer to a <a href="https://msdn.microsoft.com/72d1f049-3c8d-4332-9bf1-9f49b47cd315">NLM_CONNECTIVITY</a> enumeration value that contains  a bitmask that specifies the connectivity of this network connection.


## -returns



Returns S_OK if the method succeeds.




## -see-also




<a href="https://msdn.microsoft.com/666761b5-0146-438d-9986-ecce3b45b5ff">INetworkConnection</a>
 

 

