---
UID: NC:resapi.PEND_CONTROL_CALL
title: PEND_CONTROL_CALL
author: windows-driver-content
description: Called when a resource control code operation completes. The PEND_CONTROL_CALL type defines a pointer to this function.
old-location: mscs\endcontrolcall.htm
old-project: MsCS
ms.assetid: 0FB2C129-B98C-4570-8621-6BAD46911682
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: EndControlCall, EndControlCall callback, EndControlCall callback function [Failover Cluster], PEND_CONTROL_CALL, PEND_CONTROL_CALL callback function [Failover Cluster], mscs.endcontrolcall, resapi/EndControlCall, resapi/PEND_CONTROL_CALL
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
-	kbSyntax
api_type:
-	<TBD>
api_location:
-
api_name:
-	EndControlCall callback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PEND_CONTROL_CALL callback function


## -description


Called when a resource control code operation completes. The <b>PEND_CONTROL_CALL</b> type defines a pointer to this function.


## -parameters




### -param context [in]

The context of the call to the resource control code.

<b>Windows Server 2012 R2:  </b>Not supported.


### -param status [in]

The status of the operation.


#### - resCallId [in]

Not supported.

<b>Windows Server 2012 R2:  </b>TBD


## -returns



<b>ERROR_SUCCESS</b> if the operation is successful; otherwise, a system error code.




## -see-also




<a href="https://msdn.microsoft.com/6c7de7e6-a0f5-4308-8cf3-21968bd339a4">Resource DLL Callback Functions</a>
 

 

