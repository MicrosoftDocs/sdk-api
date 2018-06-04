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

# __MIDL___MIDL_itf_ads_0000_0000_0012 structure


## -description


The <b>ADS_REPLICAPOINTER</b> structure represents an ADSI representation of the Replica Pointer attribute syntax.


## -struct-fields




### -field ServerName

The null-terminated Unicode string that contains the name of the name server that holds the replica.


### -field ReplicaType

Type of replica: master, secondary, or read-only.


### -field ReplicaNumber

Replica identification number.


### -field Count

The number of existing replicas.


### -field ReplicaAddressHints

A network address that is a likely reference to a node leading to the name server.


## -see-also




<a href="https://msdn.microsoft.com/3ee0e469-9932-4135-8798-27d318011786">ADSI Structures</a>
 

 

