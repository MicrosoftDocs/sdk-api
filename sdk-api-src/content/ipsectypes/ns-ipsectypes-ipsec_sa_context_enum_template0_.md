---
UID: NS:ipsectypes.IPSEC_SA_CONTEXT_ENUM_TEMPLATE0_
title: IPSEC_SA_CONTEXT_ENUM_TEMPLATE0_
author: windows-sdk-content
description: Enumeration template used to enumerate security association (SA) contexts.
old-location: fwp\ipsec_sa_context_enum_template0.htm
tech.root: fwp
ms.assetid: 2e099545-4075-4ea0-9035-53ce334decc4
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IPSEC_SA_CONTEXT_ENUM_TEMPLATE0, IPSEC_SA_CONTEXT_ENUM_TEMPLATE0 structure [Filtering], IPSEC_SA_CONTEXT_ENUM_TEMPLATE0_, fwp.ipsec_sa_context_enum_template0, ipsectypes/IPSEC_SA_CONTEXT_ENUM_TEMPLATE0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ipsectypes.idl
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
 - Ipsectypes.h
api_name:
 - IPSEC_SA_CONTEXT_ENUM_TEMPLATE0
product: Windows
targetos: Windows
req.typenames: IPSEC_SA_CONTEXT_ENUM_TEMPLATE0
req.redist: 
---

# IPSEC_SA_CONTEXT_ENUM_TEMPLATE0_ structure


## -description


The <b>IPSEC_SA_CONTEXT_ENUM_TEMPLATE0</b>	structure is an enumeration template used to enumerate security association (SA) contexts.


## -struct-fields




### -field localSubNet

An <a href="https://msdn.microsoft.com/edc34005-dbc1-45a4-b6c7-fbb8b13fa388">FWP_CONDITION_VALUE0</a> structure that specifies a subnet from which SA contexts that contain a local address will be returned.  This member may be empty.

Acceptable type values for this member are: <b>FWP_UINT32</b>, <a href="https://msdn.microsoft.com/254ee02f-747d-46e4-9851-141db57e1aa7">FWP_BYTE_ARRAY16_TYPE</a>, <a href="https://msdn.microsoft.com/da6315af-264e-4dcb-b5eb-ac308128a511">FWP_V4_ADDR_AND_MASK</a>, and <a href="https://msdn.microsoft.com/d8566d41-677a-424f-89f3-e333a0520288">FWP_V6_ADDR_AND_MASK</a>.


### -field remoteSubNet

An <a href="https://msdn.microsoft.com/edc34005-dbc1-45a4-b6c7-fbb8b13fa388">FWP_CONDITION_VALUE0</a> structure that specifies a subnet from which SA contexts that contain a remote address will be returned.  This member may be empty.

Acceptable type values for this member are: <b>FWP_UINT32</b>, <a href="https://msdn.microsoft.com/254ee02f-747d-46e4-9851-141db57e1aa7">FWP_BYTE_ARRAY16_TYPE</a>, <a href="https://msdn.microsoft.com/da6315af-264e-4dcb-b5eb-ac308128a511">FWP_V4_ADDR_AND_MASK</a>, and <a href="https://msdn.microsoft.com/d8566d41-677a-424f-89f3-e333a0520288">FWP_V6_ADDR_AND_MASK</a>.


## -remarks



<b>IPSEC_SA_CONTEXT_ENUM_TEMPLATE0</b> is a specific implementation of IPSEC_SA_CONTEXT_ENUM_TEMPLATE. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/edc34005-dbc1-45a4-b6c7-fbb8b13fa388">FWP_CONDITION_VALUE0</a>
 

 

