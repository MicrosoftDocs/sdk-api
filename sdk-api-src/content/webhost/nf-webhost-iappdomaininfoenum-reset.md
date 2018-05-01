---
UID: NF:webhost.IAppDomainInfoEnum.Reset
title: Reset function
author: windows-driver-content
description: Requests a reset of the LogicalDevice.
old-location: nettcpip\cim_logicaldevice_reset.htm
old-project: NetTCPIPProv
ms.assetid: 809d81b7-d646-485f-a9c4-90957fa9546d
ms.author: windowsdriverdev
ms.date: 3/15/2018
ms.keywords: CIM_LogicalDevice class, Reset method, CIM_LogicalDevice.Reset, Reset, Reset method, Reset method, CIM_LogicalDevice class, nettcpip.cim_logicaldevice_reset
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: webhost.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: Root\standardcimv2
req.assembly: 
req.type-library: 
req.typenames: WDSTRANSPORT_TFTP_CAPABILITY, *PWDSTRANSPORT_TFTP_CAPABILITY
topic_type:
-	kbSyntax
api_type:
-	<TBD>
api_location:
-
api_name:
-	Reset method of the CIM_LogicalDevice
product: Windows
targetos: Windows
req.lib: 
req.dll: NetTCPIP.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# Reset function


## -description


Requests a reset of the LogicalDevice. The return value should be 0 if the request was successfully executed, 1 if the request is not supported and some other value if an error occurred. In a subclass, the set of possible return codes could be specified, using a ValueMap qualifier on the method. The strings to which the ValueMap contents are \'translated\' may also be specified in the subclass as a Values array qualifier.


## -parameters






## -returns



TBD




## -see-also




<a href="https://msdn.microsoft.com/11d8cbf9-264f-42b1-a0fa-be0b3a6065b9">CIM_LogicalDevice</a>
 

 

