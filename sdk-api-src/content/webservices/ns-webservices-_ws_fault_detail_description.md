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

# _WS_FAULT_DETAIL_DESCRIPTION structure


## -description



                A description of the detail element of a fault message.
            


## -struct-fields




### -field action


                    The action associated with the fault message.
                


                    If the message does not have an action, this field can be <b>NULL</b>.
                


### -field detailElementDescription


                    The description of the fault detail of the fault.  This 
                    field must be specified (it may not be <b>NULL</b>).
                


## -remarks




                The fault description defines the action of the fault message
                along with a description of the detail element that is
                contained within the fault.
            


                The fault description can be used to set and get the
                fault detail element stored within a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object
                using <a href="https://msdn.microsoft.com/469982a5-42da-40e7-a053-4820fee58828">WsSetFaultErrorDetail</a> and <a href="https://msdn.microsoft.com/426c292f-64a5-411f-a63e-6be05fe93438">WsGetFaultErrorDetail</a>.
            



