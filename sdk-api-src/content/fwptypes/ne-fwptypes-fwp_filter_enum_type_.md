---
UID: NE:fwptypes.FWP_FILTER_ENUM_TYPE_
title: FWP_FILTER_ENUM_TYPE_
author: windows-sdk-content
description: The FWP_FILTER_ENUM_TYPE enumeration type specifies how the filter enumeration conditions should be interpreted.
old-location: netvista\fwp_filter_enum_type.htm
tech.root: NetVista
ms.assetid: 4ce7a797-531c-4451-a3d5-cbf4519c185e
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: FWP_FILTER_ENUM_FULLY_CONTAINED, FWP_FILTER_ENUM_OVERLAPPING, FWP_FILTER_ENUM_TYPE, FWP_FILTER_ENUM_TYPE enumeration [Network Drivers Starting with Windows Vista], FWP_FILTER_ENUM_TYPE_, FWP_FILTER_ENUM_TYPE_MAX, fwptypes/FWP_FILTER_ENUM_FULLY_CONTAINED, fwptypes/FWP_FILTER_ENUM_OVERLAPPING, fwptypes/FWP_FILTER_ENUM_TYPE, fwptypes/FWP_FILTER_ENUM_TYPE_MAX, netvista.fwp_filter_enum_type, wfp_ref_4_enum_7cc79cf2-165c-481e-99da-33332bf13dff.xml
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: fwptypes.h
req.include-header: Fwpsk.h
req.target-type: Windows
req.target-min-winverclnt: Supported starting with  Windows Vista.
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fwptypes.h
api_name:
 - FWP_FILTER_ENUM_TYPE
product: Windows
targetos: Windows
req.typenames: FWP_FILTER_ENUM_TYPE
req.redist: 
---

# FWP_FILTER_ENUM_TYPE_ enumeration


## -description


The FWP_FILTER_ENUM_TYPE enumeration type specifies how the filter enumeration conditions should be
  interpreted.


## -enum-fields




### -field FWP_FILTER_ENUM_FULLY_CONTAINED

The function should return only filters that fully contain the enumeration
     conditions.


### -field FWP_FILTER_ENUM_OVERLAPPING

The function should return only filters that overlap with the enumeration conditions,
     including filters that are fully contained.


### -field FWP_FILTER_ENUM_TYPE_MAX

The maximum value for this enumeration. This value might change in future versions of the NDIS
     header files and binaries.

