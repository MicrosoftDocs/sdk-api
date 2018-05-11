---
UID: NF:mi.MI_DestinationOptions_GetTransport
title: MI_DestinationOptions_GetTransport function
author: windows-driver-content
description: Gets the transport setting that the client added.
old-location: wmi_v2\mi_destinationoptions_gettransport.htm
old-project: wmi_v2
ms.assetid: 85e0a952-c51c-4877-b9fb-d2fe0d0b1bb1
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: MI_DestinationOptions_GetTransport, MI_DestinationOptions_GetTransport function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_GetTransport, wmi_v2.mi_destinationoptions_gettransport
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mi.h
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
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MI_Type
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mi.h
api_name:
-	MI_DestinationOptions_GetTransport
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_DestinationOptions_GetTransport function


## -description


Gets the transport setting that the client added.


## -parameters




### -param options [in]


<a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> object returned from <a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a>.


### -param transport

A pointer to a null-terminated string that represents the returned transport setting. Supported transport setting values are listed in the <a href="https://msdn.microsoft.com/998ac6ee-29a4-49bf-8ca1-01b7afddd33f">MI_DestinationOptions_SetTransport</a> function summary.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a>



<a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a>



<a href="https://msdn.microsoft.com/998ac6ee-29a4-49bf-8ca1-01b7afddd33f">MI_DestinationOptions_SetTransport</a>
 

 

