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

# peer_pnrp_registration_info_tag structure


## -description


The <b>PEER_PNRP_REGISTRATION_INFO</b> structure contains the information provided by a peer identity when it registers with a PNRP cloud.


## -struct-fields




### -field pwzCloudName

Pointer to a Unicode string that contains the name of the PNRP cloud for which this peer identity is requesting registration. If <b>NULL</b>, the registration will be made in all clouds.  It is possible to use the special value PEER_PNRP_ALL_LINK_CLOUDS to register in all link local clouds.


### -field pwzPublishingIdentity

Pointer to a Unicode string that contains the name of the peer identity requesting registration.


### -field cAddresses

The number of SOCKADDR structures in <b>ppAddresses</b>. It is possible to use the special value PEER_PNRP_AUTO_ADDRESSES to have the infrastructure automatically choose addresses.


### -field ppAddresses

Pointer to an array of pointers to SOCKADDR structures that contain the IP addresses bound to the network interface of the peer identity requesting registration.


### -field wPort

The network interface port assigned to the address that the peer is publishing.


### -field pwzComment

Pointer to a zero-terminated Unicode string that contains a comment for this peer endpoint.


### -field payload

A <a href="https://msdn.microsoft.com/d8a8b9e3-c455-4813-b812-263efe7f5e3e">PEER_DATA</a> structure that contains a pointer to an opaque byte buffer containing application-specific data for the peer endpoint (such as a message or an image).

