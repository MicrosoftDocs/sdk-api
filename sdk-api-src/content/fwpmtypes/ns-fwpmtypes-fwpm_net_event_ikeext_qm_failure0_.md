---
UID: NS:fwpmtypes.FWPM_NET_EVENT_IKEEXT_QM_FAILURE0_
title: FWPM_NET_EVENT_IKEEXT_QM_FAILURE0_
author: windows-driver-content
description: Contains information that describes an IKE/AuthIP Quick Mode (QM) failure.
old-location: fwp\fwpm_net_event_ikeext_qm_failure0.htm
old-project: FWP
ms.assetid: a9cffcee-67a2-4a04-9ff1-85e2e02fa9a9
ms.author: windowsdriverdev
ms.date: 4/12/2018
ms.keywords: FWPM_NET_EVENT_IKEEXT_QM_FAILURE0, FWPM_NET_EVENT_IKEEXT_QM_FAILURE0 structure [Filtering], FWPM_NET_EVENT_IKEEXT_QM_FAILURE0_, fwp.fwpm_net_event_ikeext_qm_failure0, fwpmtypes/FWPM_NET_EVENT_IKEEXT_QM_FAILURE0
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FWPM_NET_EVENT_IKEEXT_QM_FAILURE0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Fwpmtypes.h
api_name:
-	FWPM_NET_EVENT_IKEEXT_QM_FAILURE0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FWPM_NET_EVENT_IKEEXT_QM_FAILURE0_ structure


## -description


The <b>FWPM_NET_EVENT_IKEEXT_QM_FAILURE0</b> structure contains information that describes an IKE/AuthIP Quick Mode (QM) failure.


## -struct-fields




### -field failureErrorCode

Windows error code for the failure.


### -field failurePoint

An <a href="https://msdn.microsoft.com/750a5643-1157-4d15-9564-127756cd08cd">IPSEC_FAILURE_POINT</a> value that indicates the IPsec state when the failure occurred.


### -field keyingModuleType

 An <a href="https://msdn.microsoft.com/a9268b07-343a-4a51-bc70-3e624facf617">IKEEXT_KEY_MODULE_TYPE</a> value that specifies the type of keying module.


### -field qmState

An <a href="https://msdn.microsoft.com/e1124447-dd56-4ab6-affc-59e351407261">IKEEXT_QM_SA_STATE</a> value that specifies the QM state when the failure occurred.


### -field saRole

An <a href="https://msdn.microsoft.com/6bb1e264-6141-4545-add5-e12f09769e25">IKEEXT_SA_ROLE</a> value that specifies the SA role when the failure occurred.


### -field saTrafficType

 An <a href="https://msdn.microsoft.com/e87154ce-7f19-424c-a577-04e2eb81560e">IPSEC_TRAFFIC_TYPE</a> value that specifies the type of traffic.


### -field qmFilterId

Quick Mode filter ID.


#### - localSubNet

An <a href="https://msdn.microsoft.com/library/windows/hardware/ff552430">FWP_CONDITION_VALUE0</a> structure that contains values that conditions can use when testing for matches.

Available when <b>saTrafficType</b> is <b>IPSEC_TRAFFIC_TYPE_TUNNEL</b>.


#### - remoteSubNet

An <a href="https://msdn.microsoft.com/library/windows/hardware/ff552430">FWP_CONDITION_VALUE0</a> structure that contains values that conditions can use when testing for matches.

Available when <b>saTrafficType</b> is <b>IPSEC_TRAFFIC_TYPE_TUNNEL</b>.


## -remarks



<b>FWPM_NET_EVENT_IKEEXT_QM_FAILURE0</b> is a specific implementation of FWPM_NET_EVENT_IKEEXT_QM_FAILURE. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

