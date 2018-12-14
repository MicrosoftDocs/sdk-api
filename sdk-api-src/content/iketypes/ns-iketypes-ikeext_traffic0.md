---
UID: NS:iketypes.IKEEXT_TRAFFIC0_
title: IKEEXT_TRAFFIC0
author: windows-sdk-content
description: Specifies the IKE/Authip traffic.
old-location: fwp\ikeext_traffic0.htm
tech.root: fwp
ms.assetid: 99cb3774-7afd-44fd-9c3e-e2d913aaeecb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IKEEXT_TRAFFIC0, IKEEXT_TRAFFIC0 structure [Filtering], fwp.ikeext_traffic0, iketypes/IKEEXT_TRAFFIC0
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
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
 - Iketypes.h
api_name:
 - IKEEXT_TRAFFIC0
product: Windows
targetos: Windows
req.typenames: IKEEXT_TRAFFIC0
req.redist: 
---

# IKEEXT_TRAFFIC0 structure


## -description


The <b>IKEEXT_TRAFFIC0</b> structure specifies the IKE/Authip traffic.


## -struct-fields




### -field ipVersion

IP version specified by <a href="https://msdn.microsoft.com/1712b83c-f32d-4981-9950-ab870a376182">FWP_IP_VERSION</a>.


### -field localV4Address

The local address of the traffic. 

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.


### -field localV6Address

The local address of the traffic. 

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V6</b>.


### -field remoteV4Address

The remote address of the traffic. 

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.


### -field remoteV6Address

The remote address of the traffic. 

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V6</b>.


### -field authIpFilterId

   Filter ID from quick mode (QM) policy of matching extended mode (EM) filter.


## -remarks



<b>IKEEXT_TRAFFIC0</b> is a specific implementation of IKEEXT_TRAFFIC. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/1712b83c-f32d-4981-9950-ab870a376182">FWP_IP_VERSION</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

