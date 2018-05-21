---
UID: NF:mi.MI_DestinationOptions_SetDestinationPort
title: MI_DestinationOptions_SetDestinationPort function
author: windows-driver-content
description: Set the port to use to communicate to the destination.
old-location: wmi_v2\mi_destinationoptions_setdestinationport.htm
old-project: wmi_v2
ms.assetid: 4359eb04-aaf7-490f-ab60-b42182b53611
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: MI_DestinationOptions_SetDestinationPort, MI_DestinationOptions_SetDestinationPort function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_SetDestinationPort, wmi_v2.mi_destinationoptions_setdestinationport
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
-	MI_DestinationOptions_SetDestinationPort
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_DestinationOptions_SetDestinationPort function


## -description


Set the port to use to communicate to the destination.


## -parameters




### -param options [in, out]

A pointer to a <a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> object returned from the <a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a> function.


### -param port

Transport port used to communicate with the server.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



Not all transports and protocols will allow the port to be changed, in which case setting this option will be ignored.  The default port used is transport-specific.




## -see-also




<a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a>



<a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a>



<a href="https://msdn.microsoft.com/49621cd8-a4ce-45b3-a20e-ecdef220d7e4">MI_DestinationOptions_GetDestinationPort</a>
 

 

