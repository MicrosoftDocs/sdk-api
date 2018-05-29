---
UID: NS:ipsectypes.IPSEC_SA_CONTEXT_ENUM_TEMPLATE0_
title: IPSEC_SA_CONTEXT_ENUM_TEMPLATE0_
author: windows-sdk-content
description: Enumeration template used to enumerate security association (SA) contexts.
old-location: fwp\ipsec_sa_context_enum_template0.htm
old-project: FWP
ms.assetid: 2e099545-4075-4ea0-9035-53ce334decc4
ms.author: windowssdkdev
ms.date: 05/08/2018
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
req.typenames: IPSEC_SA_CONTEXT_ENUM_TEMPLATE0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ipsectypes.h
api_name:
-	IPSEC_SA_CONTEXT_ENUM_TEMPLATE0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPSEC_SA_CONTEXT_ENUM_TEMPLATE0_ structure


## -description


The <b>IPSEC_SA_CONTEXT_ENUM_TEMPLATE0</b>	structure is an enumeration template used to enumerate security association (SA) contexts.


## -struct-fields




### -field localSubNet

An <a href="https://msdn.microsoft.com/library/windows/hardware/ff552430">FWP_CONDITION_VALUE0</a> structure that specifies a subnet from which SA contexts that contain a local address will be returned.  This member may be empty.

Acceptable type values for this member are: <b>FWP_UINT32</b>, <a href="https://msdn.microsoft.com/254ee02f-747d-46e4-9851-141db57e1aa7">FWP_BYTE_ARRAY16_TYPE</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff552441">FWP_V4_ADDR_AND_MASK</a>, and <a href="https://msdn.microsoft.com/library/windows/hardware/ff552446">FWP_V6_ADDR_AND_MASK</a>.


### -field remoteSubNet

An <a href="https://msdn.microsoft.com/library/windows/hardware/ff552430">FWP_CONDITION_VALUE0</a> structure that specifies a subnet from which SA contexts that contain a remote address will be returned.  This member may be empty.

Acceptable type values for this member are: <b>FWP_UINT32</b>, <a href="https://msdn.microsoft.com/254ee02f-747d-46e4-9851-141db57e1aa7">FWP_BYTE_ARRAY16_TYPE</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff552441">FWP_V4_ADDR_AND_MASK</a>, and <a href="https://msdn.microsoft.com/library/windows/hardware/ff552446">FWP_V6_ADDR_AND_MASK</a>.


## -remarks



<b>IPSEC_SA_CONTEXT_ENUM_TEMPLATE0</b> is a specific implementation of IPSEC_SA_CONTEXT_ENUM_TEMPLATE. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552430">FWP_CONDITION_VALUE0</a>
 

 

