---
UID: NS:webservices._WS_FAULT_DETAIL_DESCRIPTION
title: "_WS_FAULT_DETAIL_DESCRIPTION"
author: windows-sdk-content
description: A description of the detail element of a fault message.
old-location: wsw\ws_fault_detail_description.htm
old-project: wsw
ms.assetid: 5a89ca26-63c7-414a-a27d-019c5b020f63
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: WS_FAULT_DETAIL_DESCRIPTION, WS_FAULT_DETAIL_DESCRIPTION structure [Web Services for Windows], _WS_FAULT_DETAIL_DESCRIPTION, webservices/WS_FAULT_DETAIL_DESCRIPTION, wsw.ws_fault_detail_description
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WS_FAULT_DETAIL_DESCRIPTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_FAULT_DETAIL_DESCRIPTION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
            



