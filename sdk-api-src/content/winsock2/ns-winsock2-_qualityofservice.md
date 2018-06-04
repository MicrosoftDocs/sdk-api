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

# _QualityOfService structure


## -description


The 
<b>QOS</b> structure provides the means by which QOS-enabled applications can specify quality of service parameters for sent and received traffic on a particular flow.


## -struct-fields




### -field SendingFlowspec

Specifies QOS parameters for the sending direction of a particular flow. SendingFlowspec is sent in the form of a 
<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a> structure.


### -field ReceivingFlowspec

Specifies QOS parameters for the receiving direction of a particular flow. ReceivingFlowspec is sent in the form of a 
<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a> structure.


### -field ProviderSpecific

Pointer to a structure of type 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff565943">WSABUF</a> that can provide additional provider-specific quality of service parameters to the RSVP SP for a given flow.


## -remarks



Most applications can fulfill their quality of service requirements without using the 
<a href="https://msdn.microsoft.com/16c99de7-be29-4e58-b648-b6719385dc1c">ProviderSpecific</a> buffer. However, if the application must provide information not available with standard Windows 2000 QOS parameters, the ProviderSpecific buffer allows the application to provide additional parameters for RSVP and/or traffic control.




## -see-also




<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a>



<a href="https://msdn.microsoft.com/16c99de7-be29-4e58-b648-b6719385dc1c">ProviderSpecific Buffer</a>
 

 

