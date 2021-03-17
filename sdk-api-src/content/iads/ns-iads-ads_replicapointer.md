---
UID: NS:iads.__MIDL___MIDL_itf_ads_0000_0000_0012
title: ADS_REPLICAPOINTER (iads.h)
description: Represents an ADSI representation of the Replica Pointer attribute syntax.
helpviewer_keywords: ["*PADS_REPLICAPOINTER","ADS_REPLICAPOINTER","ADS_REPLICAPOINTER structure [ADSI]","PADS_REPLICAPOINTER","PADS_REPLICAPOINTER structure pointer [ADSI]","_ds_ads_replicapointer","adsi.ads__replicapointer","adsi.ads_replicapointer","iads/ADS_REPLICAPOINTER","iads/PADS_REPLICAPOINTER"]
old-location: adsi\ads_replicapointer.htm
tech.root: adsi
ms.assetid: f8cb8763-9533-4b80-8617-a99d75c92f07
ms.date: 12/05/2018
ms.keywords: '*PADS_REPLICAPOINTER, ADS_REPLICAPOINTER, ADS_REPLICAPOINTER structure [ADSI], PADS_REPLICAPOINTER, PADS_REPLICAPOINTER structure pointer [ADSI], _ds_ads_replicapointer, adsi.ads__replicapointer, adsi.ads_replicapointer, iads/ADS_REPLICAPOINTER, iads/PADS_REPLICAPOINTER'
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
targetos: Windows
req.typenames: ADS_REPLICAPOINTER, *PADS_REPLICAPOINTER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0000_0000_0012
 - iads/__MIDL___MIDL_itf_ads_0000_0000_0012
 - PADS_REPLICAPOINTER
 - iads/PADS_REPLICAPOINTER
 - ADS_REPLICAPOINTER
 - iads/ADS_REPLICAPOINTER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iads.h
api_name:
 - ADS_REPLICAPOINTER
---

# ADS_REPLICAPOINTER structure


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

<a href="/windows/desktop/ADSI/adsi-structures">ADSI Structures</a>