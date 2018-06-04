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

# _NL_INTERFACE_OFFLOAD_ROD structure


## -description


The <b>NL_INTERFACE_OFFLOAD_ROD</b> structure  specifies a set of flags that indicate the offload capabilities for an IP interface. 


## -struct-fields




### -field NlChecksumSupported

Type: <b>BOOLEAN</b>

The network adapter for this network interface supports the offload of IP checksum calculations.


### -field NlOptionsSupported

Type: <b>BOOLEAN</b>

The network adapter for this network interface supports the offload of IP checksum calculations for IPv4 packets with IP options.


### -field TlDatagramChecksumSupported

Type: <b>BOOLEAN</b>

The network adapter for this network interface supports the offload of UDP checksum calculations.


### -field TlStreamChecksumSupported

Type: <b>BOOLEAN</b>

The network adapter for this network interface supports the offload of TCP checksum calculations.


### -field TlStreamOptionsSupported

Type: <b>BOOLEAN</b>

The network adapter for this network interface supports the offload of TCP checksum calculations for IPv4 packets containing IP options.



### -field FastPathCompatible

 


### -field TlLargeSendOffloadSupported

Type: <b>BOOLEAN</b>

The network adapter for this network interface supports TCP Large Send Offload Version 1. With this capability, TCP can pass a buffer to be transmitted that is bigger than the maximum transmission unit (MTU) supported by the medium.  Version 1 allows TCP to pass a buffer up to 64K to be transmitted. 



### -field TlGiantSendOffloadSupported

Type: <b>BOOLEAN</b>

The network adapter for this network interface supports TCP Large Send Offload Version 2. With this capability, TCP can pass a buffer to be transmitted that is bigger than the maximum transmission unit (MTU) supported by the medium.  Version 2 allows TCP to pass a buffer up to 256K to be transmitted. 



#### - TlDatagramFastPathCompatible

Type: <b>BOOLEAN</b>

Reserved for internal use.




#### - TlStreamFastPathCompatible

Type: <b>BOOLEAN</b>

Reserved for internal use.




## -remarks



The <b>NL_INTERFACE_OFFLOAD_ROD</b> structure is defined on Windows Vista and later. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff559254">MIB_IPINTERFACE_ROW</a>
 

 

