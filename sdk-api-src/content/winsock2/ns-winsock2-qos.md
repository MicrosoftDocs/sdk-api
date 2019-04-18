---
UID: NS:winsock2._QualityOfService
title: QOS (winsock2.h)
author: windows-sdk-content
description: The QOS structure provides the means by which QOS-enabled applications can specify quality of service parameters for sent and received traffic on a particular flow.
old-location: qos\qos.htm
tech.root: QOS
ms.assetid: 859faa13-bd66-46ee-8452-6ff5d53d66c9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPQOS, LPQOS, LPQOS structure pointer [QOS], QOS, QOS structure [QOS], _gqos_qos, qos.qos, winsock2/LPQOS, winsock2/QOS"
ms.topic: struct
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Winsock2.h
api_name:
 - QOS
product: Windows
targetos: Windows
req.typenames: QOS, *LPQOS
req.redist: 
ms.custom: 19H1
---

# QOS structure


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
<a href="https://msdn.microsoft.com/a012c3ba-67fd-4fcf-84d1-85e9d495c29c">WSABUF</a> that can provide additional provider-specific quality of service parameters to the RSVP SP for a given flow.


## -remarks



Most applications can fulfill their quality of service requirements without using the 
<a href="https://msdn.microsoft.com/16c99de7-be29-4e58-b648-b6719385dc1c">ProviderSpecific</a> buffer. However, if the application must provide information not available with standard Windows 2000 QOS parameters, the ProviderSpecific buffer allows the application to provide additional parameters for RSVP and/or traffic control.




## -see-also




<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a>



<a href="https://msdn.microsoft.com/16c99de7-be29-4e58-b648-b6719385dc1c">ProviderSpecific Buffer</a>
 

 

