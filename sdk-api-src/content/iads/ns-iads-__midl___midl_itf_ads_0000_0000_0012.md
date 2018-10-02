---
UID: NS:iads.__MIDL___MIDL_itf_ads_0000_0000_0012
title: "__MIDL___MIDL_itf_ads_0000_0000_0012"
author: windows-sdk-content
description: Represents an ADSI representation of the Replica Pointer attribute syntax.
old-location: adsi\ads_replicapointer.htm
tech.root: ADSI
ms.assetid: f8cb8763-9533-4b80-8617-a99d75c92f07
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PADS_REPLICAPOINTER, ADS_REPLICAPOINTER, ADS_REPLICAPOINTER structure [ADSI], PADS_REPLICAPOINTER, PADS_REPLICAPOINTER structure pointer [ADSI], __MIDL___MIDL_itf_ads_0000_0000_0012, _ds_ads_replicapointer, adsi.ads__replicapointer, adsi.ads_replicapointer, iads/ADS_REPLICAPOINTER, iads/PADS_REPLICAPOINTER"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iads.h
api_name:
 - ADS_REPLICAPOINTER
product: Windows
targetos: Windows
req.typenames: ADS_REPLICAPOINTER, *PADS_REPLICAPOINTER
req.redist: 
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
 

 

