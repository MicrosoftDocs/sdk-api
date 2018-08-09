---
UID: NF:mi.MI_OperationOptions_SetTimeout
title: MI_OperationOptions_SetTimeout function
author: windows-sdk-content
description: Sets the operation timeout for a specific operation.
old-location: wmi_v2\mi_operationoptions_settimeout.htm
old-project: wmi_v2
ms.assetid: 73b640a4-db78-4cd2-af77-12317899d398
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: MI_OperationOptions_SetTimeout, MI_OperationOptions_SetTimeout function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_SetTimeout, wmi_v2.mi_operationoptions_settimeout
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MI_Type
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_OperationOptions_SetTimeout
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_OperationOptions_SetTimeout function


## -description


Sets the operation timeout for a specific operation.


## -parameters




### -param options [in, out]

A pointer to a <a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> structure.


### -param timeout [in]

A pointer to the new operation timeout value.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



This timeout can be set in the destination options by calling the <a href="https://msdn.microsoft.com/81309b13-657c-45fc-b4fd-21bfb28247a2">MI_DestinationOptions_SetTimeout</a> function. However, sometimes one operation may take longer than others. Therefore, it is best to set a reasonable default for all operations, then use this function to override specific operations that may take longer.

If the client is asking for progress, and the provider is reporting progress, the timeout interval will be restarted after each progress report.  For enumerations/subscribe/association, the interval is the maximum length before objects are delivered before it times out (subject to the progress comment).

If a client performs an operation (such as an invoke) on a <a href="https://msdn.microsoft.com/en-us/library/JJ819811(v=VS.85).aspx">CIM</a> session over Windows Remote Management, the operation can take longer than the operation timeout value if the target server is unreachable (for example, because of server outage, network outage, or an unexpected firewall exception). This excessive wait time occurs because the operation may be divided into suboperations for fetching schema information from the server, and the client continues continues the operation even if one or more of the schema fetch suboperations has been blocked by an unreachable server.

To mitigate this issue and get the client to report the results without an excessive wait time, try one or both of these steps:

<ul>
<li>
Set the WinRM network delay time to a very low value by invoking the following command:
<b>winrm set winrm/config/client @{NetworkDelayms="</b><i>DesiredValue</i><b>"}</b>where <i>DesiredValue</i> is the network delay value, in milliseconds. The lowest network delay that can be specified is 500 milliseconds.

The network delay value helps to account for network latency while reaching the target machine. If you set tiny network delay and operation timeout values, however, you might not be able to communicate with a target machine that takes a long time to reach. Also, a change in the network delay value affects the entire machine, not just one operation.

</li>
<li>
When starting the operation (calling a function with an "MI_Session_" prefix), specify the <b>MI_OPERATIONFLAGS_STANDARD_RTTI</b> flag in the <i>flags</i> parameter.

This changes the operation behavior so that if a fetch schema suboperation fails, the operation is aborted and completes immediately instead of waiting for subsequent fetch schema suboperations to finish. Therefore, if the server was always unreachable when the operation started, the amount of time taken by the operation to complete will be equal to the sum of the operation timeout value and the WinRM network delay value.

</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/81309b13-657c-45fc-b4fd-21bfb28247a2">MI_DestinationOptions_SetTimeout</a>



<a href="https://msdn.microsoft.com/b55e75cc-86e5-4a4e-8bb7-2fec196033cc">MI_OperationOptions_GetTimeout</a>



<a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>
 

 

