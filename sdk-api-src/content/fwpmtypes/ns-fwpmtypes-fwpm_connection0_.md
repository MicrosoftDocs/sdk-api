---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# FWPM_CONNECTION0_ structure


## -description


The <b>FWPM_CONNECTION0</b> structure stores the state associated with a connection object.


## -struct-fields




### -field connectionId

Type: <b>UINT64</b>

The run-time identifier for the connection.


### -field ipVersion

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff552435">FWP_IP_VERSION</a></b>

The IP version being used. 


### -field localV4Address

Type: <b>UINT32</b>

The IPv4 local address.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.


### -field localV6Address

Type: <b>UINT8[16]</b>

The IPv6 local address.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V6</b>.


### -field remoteV4Address

Type: <b>UINT32</b>

The IPv4 remote address.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.


### -field remoteV6Address

Type: <b>UINT8[16]</b>

The IPv6 remote address.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V6</b>.


### -field providerKey

Type: <b>GUID*</b>

Uniquely identifies the provider associated with this connection. 


### -field ipsecTrafficModeType

Type: <b><a href="https://msdn.microsoft.com/e87154ce-7f19-424c-a577-04e2eb81560e">IPSEC_TRAFFIC_TYPE</a></b>

The type of IPsec traffic.


### -field keyModuleType

Type: <b><a href="https://msdn.microsoft.com/a9268b07-343a-4a51-bc70-3e624facf617">IKEEXT_KEY_MODULE_TYPE</a></b>

The type of keying module.


### -field mmCrypto

Type: <b><a href="https://msdn.microsoft.com/59568ef7-12bd-407a-a8ee-9bf261f49883">IKEEXT_PROPOSAL0</a></b>

An IKE/AuthIP main mode proposal.


### -field mmPeer

Type: <b><a href="https://msdn.microsoft.com/b27689ef-5e2a-4163-a4d7-40f8939d4c66">IKEEXT_CREDENTIAL2</a></b>

Main mode credential information.


### -field emPeer

Type: <b><a href="https://msdn.microsoft.com/b27689ef-5e2a-4163-a4d7-40f8939d4c66">IKEEXT_CREDENTIAL2</a></b>

Extended mode credential information.


### -field bytesTransferredIn

Type: <b>UINT64</b>

The total number of incoming bytes transferred by the connection.


### -field bytesTransferredOut

Type: <b>UINT64</b>

The total number of outgoing bytes transferred by the connection.


### -field bytesTransferredTotal

Type: <b>UINT64</b>

The total number of bytes (incoming and outgoing) transferred by the connection.


### -field startSysTime

Type: <b>FILETIME</b>

Time that the connection was created.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552435">FWP_IP_VERSION</a>



<a href="https://msdn.microsoft.com/b27689ef-5e2a-4163-a4d7-40f8939d4c66">IKEEXT_CREDENTIAL2</a>



<a href="https://msdn.microsoft.com/a9268b07-343a-4a51-bc70-3e624facf617">IKEEXT_KEY_MODULE_TYPE</a>



<a href="https://msdn.microsoft.com/59568ef7-12bd-407a-a8ee-9bf261f49883">IKEEXT_PROPOSAL0</a>



<a href="https://msdn.microsoft.com/e87154ce-7f19-424c-a577-04e2eb81560e">IPSEC_TRAFFIC_TYPE</a>
 

 

