---
UID: NS:sensevts.SENS_QOCINFO
title: SENS_QOCINFO
author: windows-sdk-content
description: The SENS_QOCINFO structure is used by the ISensNetwork::ConnectionMade method. This structure contains Quality of Connection information to the sink object in an application that subscribes to SENS.
old-location: sens\sens_qocinfo.htm
old-project: Sens
ms.assetid: 33f5e790-1100-46a9-a90c-3fc51379c175
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*LPSENS_QOCINFO, SENS_QOCINFO, SENS_QOCINFO structure [SENS], _zaw_sens_qocinfo, sens.sens_qocinfo, sensevts/SENS_QOCINFO, syncmgr.sens_qocinfo"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: sensevts.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Sensevts.tlb
tech.root: 
req.typenames: SENS_QOCINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sensevts.h
api_name:
 - SENS_QOCINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# SENS_QOCINFO structure


## -description


The 
<b>SENS_QOCINFO</b> structure is used by the 
<a href="https://msdn.microsoft.com/3b067a6f-ba4c-4914-aa5b-e0fd7690e75c">ISensNetwork::ConnectionMade</a> method. This structure contains Quality of Connection information to the sink object in an application that subscribes to SENS.


## -struct-fields




### -field dwSize

This member contains the actual size of the structure that was filled in.


### -field dwFlags

Speed of connection. Flag bits indicate whether the connection is slow, medium, fast.


### -field dwOutSpeed

Speed of data sent to the destination in bits per second.


### -field dwInSpeed

Speed of data coming in from the destination in bits per second.


## -see-also




<a href="https://msdn.microsoft.com/f313588f-6257-4a0d-b95a-aabc0bc64b53">About System Event Notification Service</a>



<a href="_cos_ieventsubscription">IEventSubscription</a>



<a href="_cos_ieventsubscription_putpublisherproperty">IEventSubscription::PutPublisherProperty</a>



<a href="https://msdn.microsoft.com/3b067a6f-ba4c-4914-aa5b-e0fd7690e75c">ISensNetwork::ConnectionMade</a>
 

 

